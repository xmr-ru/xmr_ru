---
title: "Отказ от блокировки выходов на 10 блоков"
date: "2022-01-02"
categories:
  - "Новости"
tags:
  - ""
lead: "Это предложение по отказу от блокировки выходов на 10 блоков, используемой Monero и не позволяющей пользователям тратить выходы до тех пор, пока сетью не будет принято ещё 10 блоков."
pager: true
toc: false
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

У данного предложения имеется два значительных и очевидных недостатка, но я считаю, что с учётом всех ограничений это наилучшее из решений.

Если вы читаете это предложение, пожалуйста, перед тем как забыть о нём навсегда, сначала рассмотрите его с академической точки зрения. Да, действительно, недостатки могут показаться вам довольно серьёзными, но до вынесения окончательного приговора мне бы хотелось, чтобы предложение стало предметом конструктивного обсуждения.

## _Причины, по которым существует блокировка на 10 блоков_

С моей точки зрения, существует одна основная причина, по которой мы в Monero используем блокировку выходов на 10 блоков.

Выходы в «зоне reorg» доказательства работы (примерно от 1 до 10 последних блоков) могут быть полностью удалены из блокчейна при выполнении операции reorg, поскольку любой выход, к которому будет применима эта операция, точно так же можно и потратить дважды. Если злоумышленник произведёт атаку на сеть путём двойной траты своих собственных выходов, то «естественным образом» регулярная операция reorg станет причиной того, что некоторые из его транзакций будут заменены двойной тратой входов этих транзакций. Если выход, созданный первой группой, будет использоваться в качестве ложного случайным пользователем, то транзакция такого пользователя станет недействительной после выполнения операции reorg.

Другими словами, ложные выходы уязвимы с точки зрения проблемы «подтверждения». Автору транзакции следует использовать только «строго подтверждённые» ложные выходы, то есть те, которые находятся ниже «зоны reorg».

Поскольку для создания транзакций требуются строго подтверждённые ложные выходы, выходы в «зоне reorg» никогда не будут использоваться в качестве ложных. Следовательно, любой выход из «зоны reorg», на который указывает кольцевая подпись входа транзакции, и будет реально расходуемым выходом для такого входа. Автора транзакции может и не смущать, что его реально расходуемый выход будет раскрыт. Однако если этот выход будет использован в качестве ложного в транзакциях других пользователей, то, поскольку внешнему наблюдателю будет известно, что он был потрачен, такой наблюдатель также будет знать и то, что это тоже ложный выход и в транзакциях других пользователей. Это делает кольцевые подписи, создаваемые этими пользователями, более уязвимыми. Во избежание подобного ослабления защиты и была введена блокировка выходов на 10 блоков. Благодаря этому все ложные выходы, соответствующие входу транзакции, вероятно, могут являться реальными.

## _Предложение_

1. Разрешить включать в транзакции входы с нулевым количеством ложных выходов, если такие входы являются совсем недавними (если они были недавно добавлены в блокчейн).
2. По истечении периода отсрочки удалять выходы из пула, соответствующие критериям участников кольца, если они были потрачены со входом с нулевым количеством ложных выходов.

Это обеспечит компромисс между скоростью траты и минимизацией ущерба, который может вызвать быстрая трата с точки зрения эффективности кольцевой подписи.

```
// constants
DEFAULT_SPENDABLE_AGE = 10;
INPUT_ELIGIBILITY_GRACE_BLOCKS = 20;
ZERO_DECOY_ELIGIBLE_ZONE = DEFAULT_SPENDABLE_AGE + INPUT_ELIGIBILITY_GRACE_BLOCKS;  //30
PROVABLY_SPENT_DECOY_ELIGIBLE_ZONE = ZERO_DECOY_ELIGIBLE_ZONE + INPUT_ELIGIBILITY_GRACE_BLOCKS; //50

fn validate_input_age_zero_decoy(block_height, input_height) -> bool
{
    // only outputs in the zero-decoy eligible zone can be spent with zero decoys
    if (block_height - input_height > ZERO_DECOY_ELIGIBLE_ZONE)
        return false;
    else
        return true;
}

fn validate_input_age(block_height, input_height, input) -> bool
{
    // only outputs that reached the default spendable age can be referenced in a membership proof with > 0 decoys (IF they are not 'provably spent and older than the provably spent eligible zone')
    if (block_height - input_height <= DEFAULT_SPENDABLE_AGE ||
        (block_height - input_height > PROVABLY_SPENT_DECOY_ELIGIBLE_ZONE && is_provably_spent(input))
        )
        return false;
    else
        return true;
}
```

## _Зачем нужен период отсрочки?_

Транзакция, попадающая в пул транзакций, не может быть добавлена в блок немедленно. Если в транзакции будет потрачен вход с нулевым количеством ложных выходов и этот вход будет создан за 10 блоков до момента построения транзакции, при отсутствии периода отсрочки его нельзя будет добавить даже в формируемый на тот момент блок.

Если транзакция с нормальным входом указывает на доказуемо потраченный вход, появившийся 20 блоков назад и, вероятно, потраченный в транзакции, проведённой 10 блоков назад, то он не может быть добавлен в формируемый блок без периода отсрочки для доказуемо потраченных участников кольца.

При построении транзакции, если реально расходуемый выход находится в пределах блокировки на 10 блоков, то он тратится в качестве входа с нулевым количеством ложных выходов. В противном случае кольцевая подпись строится как обычно (однако автору транзакции следует избегать использования ложных выходов, которые, вероятно, уже были потрачены). «Отсроченными» блоками не следует злоупотреблять при создании входов с нулевым количеством ложных выходов старше 10 блоков.

## _Недостатки_

У этого предложения есть два основных недостатка:
1. При построении транзакции любые ложные выходы, выбранные из последних соответствующих всем требованиям 20 блоков, могут стать доказуемо потраченными.
2. Поскольку приемлемость по типу входов меняется как функция высоты блока, в котором добавляется транзакция, если такая транзакция задерживается в пуле транзакций на время, превышающее период отсрочки, составляющий 20 блоков, она может стать недействительной.
  - Любая транзакция со входом с нулевым количеством ложных выходов станет недействительной.
  - Любая транзакция с нормальным входом, указывающая на доказуемо потраченный выход, станет недействительной. В случае реализации детерминированного биннинга детерминированные ссылки по границе приемлемости могут не работать (из-за того, что после удаления доказуемо потраченных выходов порядок/индексирование выходов в блоках изменится). В этом случае транзакции с нормальными входами всегда будут становиться недействительными по окончании периода отсрочки.

Следует отметить, что делегирование доказательства участия в рамках протокола Seraphis всегда позволяет авторам транзакций завершить доказательства участия непосредственно перед передачей их транзакций, что делает «медленные» транзакции, подобные тем, что строятся по схеме multisig или при проведении атомных свопов, совместимыми с данным предложением (в противном случае период отсрочки, как правило, истекал бы ещё до того, как транзакцию можно было бы передать для включения в блокчейн).

## _Взгляд в будущее_

Если бы в Monero было реализовано идеальное доказательство участия, которое бы указывало на все выходы в блокчейне, то и воплощение данного предложения значительно упростилось бы за счёт возможности «использования входов с нулевым количеством ложных выходов в том случае, если такие входы были созданы менее чем 30 блоков назад».

---

_Источник: [Eliminating the 10-block-lock #95](https://github.com/monero-project/research-lab/issues/95)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
