---
title: "Номиналы в Monero"
categories:
  - "Руководства"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

Полного руководства по использованию M/N multisig-кошельков Monero пока не существует, так как это довольно новая схема. Данное руководство призвано собрать воедино всю информацию, необходимую для использования схемы M/N мультиподписей (multisig).

Multisig-кошельки очень важны для тех людей и организаций, которым необходима возможность безопасного хранения криптовалют. Такие кошельки защищены приватными ключами от кражи, а на случай потери предусмотрено резервирование. Multisig-кошельки являются стандартным средством обеспечения безопасности, используемым множеством бирж, сетевых кошельков, криптофондов, обычных фондовых организаций и других финансовых институтов, которым приходится иметь дело с большими объёмами криптовалюты.

Этот пост будет посвящён Monero, хотя большинство людей, вероятно, впервые столкнулось с multisig-адресами, когда речь заходила о Bitcoin. Механизм работы Monero сильно отличается от механизма Bitcoin, поэтому разработчиками Moneroбыла предложена новая система реализации мультиподписей. Такая система не должна была зависеть от языка описания Bitcoin и должна была достаточно хорошо взаимодействовать с криптосистемами, которые использует Moneroдля обеспечения анонимности своих пользователей.

Реализация мультиподписейMoneroпроисходила в два этапа. Сначала, в конце 2017 года, были предложены N/N и N-1/N мультиподписи, которые позволили использовать мультиподписи кошельков по схемам «2 из 2» и «2 из 3». Затем, в конце 2018 года, были предложены кошельки Monero, использующие схему M/N, в которой произвольное значение M должно быть меньше N. Сюда относятся схемы «3 из 5».

Давайте начнём с первоначальной настройки multisig-кошелька Monero.

## _Настройка multisig-кошелька Monero​_

*Отказ от ответственности*. В одной из версий реализации схемы мультиподписей M/N был обнаружен [баг](https://github.com/monero-project/monero/issues/4793), который иногда не позволял тратить с кошельков, использующих схему M/N. Ошибка была исправлена после выхода последней версии Monero (v0.13.0.4), поэтому следует проверить последовательность выполнения операций вашим кошельком перед тем, как сохранять в нём значительные средства. Надёжность процесса, описанного в данном руководстве, была проверена на главной ветви разработки Monero.

Ручная настройка multisig-кошелька в случае с Moneroявляется трудоёмким процессом, поскольку кошелькам, принимающим в нём участие, необходимо в несколько заходов обменяться друг с другом данными, чтобы создать multisig-ключи, которые необходимы для того, чтобы видеть и подписывать транзакции. Для каждого из трёх типов кошельков есть свой процесс настройки: N/N, N-1/N и M/N. Из этих трёх M/N является самым сложным, так как настройка по схеме «3 из 5» требует совершения кошельком 25 операций. Я считаю, что с точки зрения экономии времени и во избежание ошибок, проще всего было бы автоматизировать процесс.

При любой настройке мультиподписей среди программ Monero с поддержкой командной строки будет утилита для генерирования кошельков с названием monero-gen-trusted-multisig. Если вы хотите сгенерировать все участвующие multisig-кошельки на одной проверенной машине, программа сделает всё за вас. Утилиту, настраивающую нужную вам схему, можно вызвать следующим образом:

`$ monero-gen-trusted-multisig --scheme=3/5 --filename-base=wallet`

Если это не подходит для вашего случая, то процесс настройки несколько усложнится. В этом документе нами предлагается краткий обзор процесса для каждого типа схемы, но подробно мы рассматриваем только схему для M/N кошельков (для схемы N/N и N-1/N кошельков уже имеется [хорошее руководство](https://monero.stackexchange.com/questions/5646/how-to-use-monero-multisignature-wallets-2-2-2-3)).

Ниже приводятся команды, необходимые, чтобы сгенерировать multisig-кошелёк каждого типа. Эти команды можно вводить либо используя командную строку программы monero-wallet-cli, либо при помощи JSON-RPC сервера monero-wallet-rpc. Каждая команда запускается единожды для каждого участвующего в процессе кошелька. Параметры каждой команды указаны в [Руководстве по RPC кошелька Monero](https://www.getmonero.org/resources/developer-guides/wallet-rpc.html).

Следует убедиться в том, что для создания multisig-кошелька используются новые или пустые кошельки. Если вы преобразуете использующий одну подпись кошелёк с имеющимися в нём средствами в multisig-кошелёк, средства будут потеряны.

*Настройка кошелька по схеме N/N*:
1. create_wallet
2. prepare_multisig
3. make_multisig

*Настройка кошелька по схеме N-1/N*:
1. create_wallet
2. prepare_multisig
3. make_multisig
4. finalize_multisig

## _Настройка кошелька по схеме M/N​_

1. create_wallet
2. prepare_multisig
3. make_multisig
4. exchange_multisig_data (множество раундов)

### _Подробности настройки по схеме M/N_

Так как настройка по схеме M/N предполагает наличие множества шагов, нами будут указаны команды, использующие JSON-RPC API, которые позволят автоматизировать процесс при помощи скрипта. Если вы производите операции с кошельком, используя monero-wallet-rpc, то при запуске вам придётся пройти опцию —wallet-dir.

1. create_wallet (N раз)
2. prepare_wallet (N раз для каждого кошелька)
3. make_multisig (N раз для каждого кошелька)
4. exchange_multisig_data (M-Nраундов по N раз для каждого кошелька)
5. [опционально] is_multisig

#### _1. Создание кошельков​_

Сначала следует создать N-кошельков, которые станут участниками multisig-кошелька.

_Запрос_:

```
{
   "jsonrpc": "2.0",
   "id": "0",
   "method": "create_wallet",
   "params": {
       "filename": "wallet_0",
       "password": "",
       "language": "English"
   }
}
```

_Ответ_:

```
{
   "id": "0",
   "jsonrpc": "2.0",
   "result": {}
}
```

#### _2. Подготовка multisig-кошелька​_

Затем необходимо собрать multisig-данные первого раунда для каждого кошелька. Понадобится сохранить поле возврата данных multisig_info. Примечание: если процесс будет полностью автоматизирован при помощи API, перед каждым очередным вызовом prepare_multisig также может понадобиться ввод команд close_wallet и open_wallet. В данном случае мы опускаем их из соображений краткости изложения.

_Запрос_:

```
{
   "jsonrpc": "2.0",
   "id": "0",
   "method": "prepare_multisig"
}
```

_Ответ_:

```
{
   "id": "0",
   "jsonrpc": "2.0",
   "result": {
       "multisig_info": "MultisigV1aFJ22AwxbBW6YkJH9…"
   }
}
```

#### _3. Реализация multisig-кошелька​_

Команда make_multisig изменяет каждый кошелёк, делая его multisig-кошельком. Она применяется к каждому кошельку-участнику схемы multisig. Команда make_multisig использует два параметра:

1. multisig_info, который является матрицей возврата данных multisig_info прошлого этапа для всех остальных кошельков, за исключением того кошелька, на котором производится операция.
2. Порог, являющийся тем количеством кошельков, которое необходимо для подписания и отправки транзакции (значение M в схеме «M из N»).

Как и в случае с командой prepare_multisig, make_multisig также возвращает данные, которые необходимо сохранить и использовать при выполнении последующих шагов.

_Запрос_:

```
{
   "jsonrpc": "2.0",
   "id": "0",
   "method": "make_multisig",
   "params": {
       "multisig_info": [
           "MultisigV1E1s9eCf4kWDa282j9f…",
           "MultisigV1NahETBVSqVtdbfZ4hz…",
           "MultisigV1SQWPjeNuJKyHT88KA2…",
           "MultisigV1i1UZiz3KtxQSwWReGR…"
       ],
       "threshold": 3
   }
}
```

_Ответ_:

```
{
   "id": "0",
   "jsonrpc": "2.0",
   "result": {
       "address": "41fJjQDhryD11111111111111111111111…...",
       "multisig_info": "MultisigxV1KUADv8n3GBJCrpDu…..."
   }
}
```

#### _4. Обмен multisig-ключами​_

Последний этап создания multisig-кошелька запускается командой exchange_multisig_keys. Команда в качестве параметра использует multisig_info, который является матрицей возвращённых значений multisig_info прошлого этапа для всех остальных кошельков. Возвращённое значение также включает в себя ещё одно поле multisig_info, которое необходимо сохранить для использования в будущем.

В зависимости от настройки вашего кошелька, понадобится множество раундов обмена ключами (exchange_multisig_keys). Для схемы мультиподписей M/N понадобится от N до M раундов. Так, например, если вы настраиваете кошелёк по схеме «3 из 5», то понадобится 5−3 = 2 раунда. В каждом раунде возвращённые значения multisig_info других кошельков должны использоваться в качестве параметров. В последнем раунде возвращённое значение будет multisig_info представлено пустой строкой.

_Запрос_:

```
{
   "jsonrpc": "2.0",
   "id": "0",
   "method": "exchange_multisig_keys",
   "params": {
       "multisig_info": [
           "MultisigxV1KUADv8n3GBJCrpDuavNpaPT…",
           "MultisigxV1TJyJjqRwEuPePPE8PuNBLmB…",
           "MultisigxV1jZvNKUnrGsSS85qQiSCs6i3…",
           "MultisigxV16KauRuvCPekZEHdDgjP8Jhf…"
       ]
   }
}
```

_Ответ_:

```
{
   "id": "0",
   "jsonrpc": "2.0",
   "result": {
       "address": "",
       "multisig_info": "MultisigxV1dXxJPiqpUNSU2DjLmX8Ct…"
   }
}
```

#### _5. Проверка multisig-статуса кошелька (опционально)​_

В конце процесса настройки можно запустить выполнение команды is_multisig, предназначенной для проверки правильности настройки. Команда вернёт объект JSON, а затем сообщит multisig-статус кошелька.

_Запрос_:

```
{
   "jsonrpc": "2.0",
   "id": "0",
   "method": "is_multisig"
}
```

_Ответ_:

```
{
   "id": "0",
   "jsonrpc": "2.0",
   "result": {
       "multisig": true,
       "ready": true,
       "threshold": 3,
       "total": 5
   }
}
```

### _Трата средств с ваших кошельков​_

Надеюсь, команда is_multisig порадовала вас, сообщив, что все ваши кошельки настроены и готовы к использованию. Пришло время использовать их.

Процесс траты средств с M/N multisig-кошелька такой же, как в случае с multisig-кошельками другого типа. Поэтому вы можете воспользоваться [руководством для N/N и N-1/N](https://monero.stackexchange.com/questions/5646/how-to-use-monero-multisignature-wallets-2-2-2-3).

Единственной особенностью траты при помощи JSON-API является возможная ошибка отсутствия LRдля достаточного количества участников. В этом случае кошелькам, участвующим в транзакции, необходимо использовать команду refresh до вызова export_multisig_info. Если же вы использовали программу с командной строкой, она сообщит вам о необходимости ввода refresh, когда понадобится. В случае использования JSON-API необходимо знать, что для устранения этой ошибки требуется refresh.

## _Заключение​_

Ну, вот и всё! Возможно, вас немного напугало количество шагов, описанных здесь, особенно, если вы попытаетесь координировать обмен данными между несколькими различными машинами. К счастью, члены сообщества Moneroработают над программным обеспечением, которое упростит процесс настройки multisig-кошельков. MoneroMessagingSystem (MMS), которая в настоящее время тестируется, повысит уровень автоматизации такой настройки и обеспечит безопасность передачи данных мультиподписей между машинами.

Я надеюсь, что это руководство поможет вам использовать мультиподписи с Monero.
