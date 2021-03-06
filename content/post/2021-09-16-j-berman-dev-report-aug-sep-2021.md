---
title: "Отчёт j-berman за август/сентябрь по разработке и интеграциям"
date: "2021-10-08"
categories:
  - "Новости"
tags:
  - "CCS"
lead: "Ежемесячный отчёт j-berman в ключе работы над его CCS предложением."
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

_30 августа — 12 сентября_
_Рабочее время: 93 часа ([CCS_1_time_tracking_weeks_1-2.ods](https://repo.getmonero.org/monero-project/ccs-proposals/uploads/b9ec215e6ab11e3a64f9017051970210/CCS_1_time_tracking_weeks_1-2.ods))_

## _Аннотация_

Во-первых, хотелось бы отметить, что я очень взволнован и испытываю больше, чем простой восторг, от получения возможности поработать в своей любимой области. Я крайне признателен сообществу Monero за полученный шанс, и я сделаю всё возможное, чтобы принести максимальную пользу проекту Monero. Я работаю и прилагаю все свои силы для выполнения поставленной задачи.

Во-вторых, я также отмечу, что не быль столь продуктивен, насколько надеялся, в течение первой пары недель, но я быстро нагоняю упущенное. Я уверен, что к моменту публикации следующего отчёта в конце первого месяца моей работы результаты будут гораздо лучше. Я также решил сфокусироваться исключительно в рамках настоящего предложения CCS и не стану браться за какую-либо другую работу, по крайней мере, пока не закончу с этой.

## _Чем я занимался последние две недели_

- Непрерывный анализ алгоритма выбора ложных выходов и [рекомендованное исправление ошибки отсечения целых частей в wallet2](https://github.com/monero-project/monero/pull/7798#issuecomment-917495021), которое было необходимо внести до выхода следующей версии (это было пунктом №1 в контексте улучшения алгоритма выбора ложных выходов).
    - [Дополнительный анализ алгоритмов выбора ложных выходов MyMonero+monero-lws и openmonero](https://github.com/monero-project/research-lab/issues/86#issuecomment-915806414) в соответствии с [критическими замечаниями](https://github.com/monero-project/research-lab/issues/86#issuecomment-915581533) со стороны vtnerd в отношении моих (слишком правдоподобных) выводов, согласно которым реальные выходы, вероятно, можно идентифицировать.
- [Ретроспективный анализ ошибок в алгоритме выбора ложных выходов](https://github.com/monero-project/monero-site/pull/1831).
    - ВАЖНОЕ ПРИМЕЧАНИЕ. В ходе проверки корректности алгоритма выбора ложных выходов monero-lws, которая должна была показать, работает ли алгоритм так, как ему положено, я понял, что ошибки, связанной с выбором ложных выходов, о которой так много говорилось, не было. А это означает, что ставшая известной ошибка с выбором ложных выходов, которая заключалась в том, что недавно созданные выходы можно было без труда идентифицировать, по сути, не является таковой, поскольку пользователи MyMonero (и monero-lws) вполне могли строить транзакции, используя в качестве ложных выходов те, что были созданы гораздо раньше. Я связался с командой MyMonero месяц назад или около того, чтобы разобраться с тем, какой вариант реализации они используют, и выяснил, что это monero-lws, но в тот момент я ещё не понимал, что в коде не было той же ошибки.
- [Помощь в обновлении monero-lws в целях соответствия этой реализации версии 0.17.2.3 Monero](https://github.com/vtnerd/monero-lws/issues/19#issuecomment-911300158).
- [Подача запроса PR с целью адаптации алгоритма выбора ложных выходов monero-lws к алгоритму wallet2](https://github.com/vtnerd/monero-lws/pull/22).
    - Хоть и задним числом, но, с учётом критических замечаний vtnerd, стало очевидным, что мне следовало сначала заняться отсечением целых частей в wallet2, а затем уже подавать данный запрос PR.
- Подача запроса PR с целью повышения безопасности ветви ряда функций RPC демона.
    - [PR, направленный на повышение безонасности ветви функций строго считывающих (но не пишущих) LMDB](https://github.com/monero-project/monero/pull/7936).
    - Пока я работал над этим PR, мною была обнаружена и исправлена незначительная ошибка в on_getblockhash, которая заключалась в отсутствии сообщения об ошибке, если запрошенная высота превышала высоту блокчейна. Также я обнаружил небольшую ошибку в on_get_transactions, которая будет исправлена в будущем.
    - PR, направленный на повышение безопасности ветви всего пула.
- Я начал ознакомление с monero-lws и проработал концепцию аудита.
    - Мною рассматривается возможность реализации подадресов в monero-lws (более подробно об этом написано ниже).
    - Принял участие в обсуждении аномального роста размера транзакций, начиная с [конца июля](https://bitinfocharts.com/comparison/monero-transactions.html#3m).
    - Я ознакомился с запросом PR, представленным Sech1 ([обновление monerod для p2pool](https://github.com/monero-project/monero/pull/7891)), а также с запросов ndorf по обновлению REST API сервера lightwallet, которое позволит [находить только новые транзакции, которые ещё не знакомы клиенту](https://github.com/monero-project/meta/pull/603).

## _Чем я планирую заниматься ближайшие две недели_

_Дальнейшее рассмотрение возможности реализации биннинга с целью улучшения алгоритма выбора ложных выходов_

Напомню: биннингом называют стратегию выбора ложных выходов в «бинах» примерно одного возраста, что решает проблему алгоритма выбора ложных выходов.

UkoeHB [поднял вопрос](https://github.com/monero-project/research-lab/issues/78#issuecomment-913046076), связанный со временем блокировки, негативно влияющим на биннинг. Злоумышленник вполне может создать множество выходов, которые будут заблокированы, а это приведёт к нежелательному эффекту, который непременно скажется на биннинге:

> Что если локальные все выходы, окружающие выход, который вы хотите потратить, окажутся заблокированными? Может статься так, что в бине не окажется достаточного количества ложных выходов, чтобы потратить реальный выход. И это создаёт серьёзный вектор атаки.

UkoeHB выделил три возможных варианта решения проблемы: удаление времени блокировки, шифрование времени блокировки, или же использование только незаблокированных ложных выходов (что также создаёт вектор атаки, так как кто-нибудь может медленно накопить ряд выходов, которые будут разблокированы в определённое время, для проведения, например, флуд-атаки). Решение проблемы времени блокировки, на мой взгляд, на данный момент состоит в создании блокировщика для биннинга. Поэтому я инициировал обсуждение этого вопроса на сегодняшней [встрече MRL](https://github.com/monero-project/meta/issues/610) и продолжу подталкивать сообщество к решению этой проблемы в дальнейшем. Поскольку консенсус по этому вопросу уже практически достигнут (по крайней мере, выглядит всё именно так), я стану посвящать больше времени реализации биннинга.

_**Неформальный аудит monero-lws**_

На раннем этапе vtnerd упомянул, что ему хотелось бы, чтобы кто-нибудь посмотрел и попытался найти возможные бэкдоры, которые могут навредить приватности. Я займусь этим и даже сделаю немного больше.

Вот модель угрозы, которую я буду оценивать: пользователь, использующий monerod + monero-lws на сервере, доступ к которому есть только у него во избежание утечки информации о транзакциях Monero третьей стороне, при нормальных условиях. Примеры утечки могут быть следующими:
- бэкдор, отправляющий чувствительные данные monero-lws третьей стороне vtnerd/a;
- get_random_outs, выдающий ложные выходы, компрометирующие транзакции пользователя, когда те сохраняются в блокчейне;
- запросы API обменного курса могут раскрыть информацию поставщику услуг.

Если честно, я не думаю, что мне удастся выявить какие-либо уязвимости в рамках вышеуказанной модели угрозы — я уже провёл некоторое время за изучением кода. Чтобы вселить уверенность в результатах аудита я собираюсь прочитать каждую строку в каждом файле и разъяснить суть критически важных файлов и функций. Результаты будут соответствующим образом задокументированы.

Я также собираюсь рассмотреть более широкую модель угрозы: в идеале раскрытие вашей monero-lws в Интернете не позволит кому-либо получить пользовательскую информацию с сервера. Это означает, что только владелец адреса/ключа просмотра сможет увидеть транзакции, сохранённые на сервере.

_**Обновление openmonero и monero-lws в целях обеспечения соответствия алгоритму выбора ложных выходов wallet2**_

Перед обновлением следует дождаться, что будет решено по вопросу wallet2 согласно [этому запросу PR](https://github.com/monero-project/monero/pull/7798#issuecomment-917495021).

_**Продолжение работы над безопасностью ветви в RPC демона**_

Есть ещё функции, требующие доработки, чтобы сделать ветвь безопасной. Я немного рассказываю об этом [в данном запросе PR](https://github.com/monero-project/monero/pull/7936).

_**Реализация поддержки подадресов в monero-lws**_

Я провёл некоторое время за рассмотрением этой проблемы по запросу @CryptoGrampy и продолжу заниматься этим в дальнейшем. Не думаю, что реализовать поддержку в monero-lws будет сложно (технически всё должно «работать» при наличии правильно помещённых комментариев, но адрес, который вы будете видеть в CLI будет неправильным). По моей начальной оценке эта работа должна занять у меня две недели или около того (при этом мне придётся ускориться с работой в кодовой базе), но я уверен, что у vtnerd есть более удачная идея. Я также начал обсуждение вопроса с Девином из MyMonero, и мы с vtnerd можем поработать с ребятами из MyMonero над решением проблемы (особенно если кто-то из них решит, что было бы неплохо немного изменить API, но, как по мне, этого не понадобится).

Кажется, над поддержкой monero-lws будет работать немало людей, и лично я в целом буду рад по возможности помочь vtnerd.

---

_Источник: [j-berman full-time development (3 months)](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/249#note_11480)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
