---
title: "The Monero Moon (выпуск 42)"
date: "2022-05-12"
categories:
  - "Новости"
tags:
  - "Monero Moon"
lead: "The Monero Moon — это курируемый еженедельный информационный бюллетень обо всём, что касается Monero."
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

### _Разработка, новые версии и технологии_

В рамках подготовки к июльскому обновлению сети Monero разработчиками на 16 мая 2022 г. был запланирован хардфорк в тестовой сети Monero. Хардфорк будет реализован на высоте блока 1 982 800 и 1 983 520. Этот вопрос обсуждался на последней встрече разработчиков, состоявшейся 7 мая и подробно освещённой Monero Observer. Разработчики обсудили соответствующие даты обновления сети и обновления multisig. С кратким описанием или «сырым» протоколом встречи можно ознакомиться [здесь](https://www.monero.observer/meeting-log-summary-monero-development-workgroup-meeting-7-may-2022/).

![01](/img/post/2022-05-12-the-monero-moon-42/01.png)  
*https://www.monero.observer/meeting-log-summary-monero-development-workgroup-meeting-7-may-2022/*

В основной сети появилось приложение Shruum Wallet форка Monerujo с дополнительными механизмами, обеспечивающими безопасность, а также добавлением и удалением некоторых функций. Среди особенностей кошелька Shruum следует отметить обязательное использование Tor, отсутствие поддержки Sideshift, обязательное использование паролей, а также поддержку Ledger Nano S Plus. Скачать приложение можно на их [веб-сайте](https://mayumi.one/). Прочую информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ujwiag/shruum_wallet_mainnet_apk_released_a_monerujo/).

![02](/img/post/2022-05-12-the-monero-moon-42/02.png)  
*https://www.reddit.com/r/Monero/comments/ujwiag/shruum_wallet_mainnet_apk_released_a_monerujo/*

[binarybaron](https://github.com/UnstoppableSwap/unstoppableswap-gui/commits?author=binarybaron) опубликовал версию v0.3.0 UnstoppableSwap GUI, позволяющего совершать не требующие доверительных настроек атомные свопы XMR-BTC. В рамках обновления был интегрирован Tor и добавлены ярлыки в текстовых полях адресов Monero и Bitcoin.

![03](/img/post/2022-05-12-the-monero-moon-42/03.png)  
*https://github.com/UnstoppableSwap/unstoppableswap-gui/releases/tag/v0.3.0*

AnonimaUzanto создал утилиту для считывания данных напрямую из базы Monero исключительно с помощью Python. Утилита не требует наличия демона и какого-либо кода Monero. Программу можно найти [здесь](https://www.reddit.com/r/Monero/comments/uinzvk/python_monero_database_reader/).

![04](/img/post/2022-05-12-the-monero-moon-42/04.png)  
*https://github.com/AnonimaUzanto/py-monerodb*

Контрибьютор Monero Говард Чу (Howard Chu) работает над добавлением поддержки ARM MacOSX во воспроизводимые сборки Monero. Соответствующую информацию можно получить, ознакомившись с [этим постом](https://github.com/monero-project/monero/pull/8312) или твитом, размещённым ниже.

![05](/img/post/2022-05-12-the-monero-moon-42/05.png)  

Gingeropolous опубликовал в системе CCS предложение по сборке, поддержке и администрированию high-end серверов, которые позволят облегчить и улучшить процесс разработки и исследования Monero! С предложением можно ознакомиться [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/317).

mj-xmr опубликовал отчёт по разработке за апрель и май. В нём подробно рассказывается о таких вещах, как алгоритм выбора ложных выходов Monero. Обязательно ознакомьтесь с [этим отчётом](https://www.reddit.com/r/Monero/comments/umgew1/mjs_dev_report_aprmay_2022_23/).

ditatompel поделился списком удалённых узлов Monero с публичным API (json). Список можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ul0jsd/public_api_monero_remote_node_list_json/).

![06](/img/post/2022-05-12-the-monero-moon-42/06.png)  
*https://www.reddit.com/r/Monero/comments/ul0jsd/public_api_monero_remote_node_list_json/*

Сообщество Monero [выразило озабоченность](https://www.reddit.com/r/Monero/comments/uk8pab/always_stop_mining_on_minexmr_currently_at_39_of/) в отношении получения пулом minexmr значительного процента от общего хешрейта. На момент написания данного бюллетеня на пул приходилось более 40% известного хешрейта. Майнеров призывают приостановить майнинга на minexmr.com, чтобы обеспечить децентрализованность глобальной сети. Список альтернативных пулов можно найти по следующей ссылке: miningpoolstats.stream/monero.

![07](/img/post/2022-05-12-the-monero-moon-42/07.png)  
*https://minexmr.com/pools.html*

NOWnodes опубликовал [руководство](https://nownodes.io/blog/how-to-run-monero-node/), которое научит пользователей, как создать собственный узел Monero.

Для создания узла также можно воспользоваться официальным GUI-кошельком Monero!

![08](/img/post/2022-05-12-the-monero-moon-42/08.png)  

Команда Monero Talk поделилась видео с конференции Monerotopia с участием Арона Фиккерта (Aaron Feickert), также известного как Sarang Noether, исследователя XMR, в котором он поделился своими мыслями относительно аудита денежной массы.

{{< youtube id="aHv2gq4Wm5I" autoplay="false" >}}  

Также стоит посмотреть и другое видео с Monerotopia с участием контрибьютора Monero, ведущего разработчика проекта Seraphis, а также автора книги «Monero с нуля» - Koe.

{{< youtube id="XbMLK-aarKU" autoplay="false" >}}  

Посмотрите на эти старые графики 2016 года и сравните объём эмиссии и размер вознаграждения за вычисление блока Monero и Bitcoin.

![09](/img/post/2022-05-12-the-monero-moon-42/09.png)  
*https://imgur.com/a/De0G2*

Сообщаем о выходе версии v13.1.0 MMGen (Multi-Mode GENerator), онлайн/офлайн криптовалютного кошелька с поддержкой командной строки. Дополнительную информацию можно получить, ознакомившись [с этим постом](https://www.reddit.com/r/Monero/comments/un81wo/announcing_version_1310_of_the_mmgen_commandline/).

Feather Wallet изменили свой логотип и ждут отзывов от сообщества Monero. Более полную информацию можно найти [здесь](https://www.reddit.com/r/FeatherWallet/comments/umgojt/feather_wallet_logo_redesign_feedback_wanted/).

![10](/img/post/2022-05-12-the-monero-moon-42/10.jpeg)  
*Один из возможных логотипов - https://www.reddit.com/r/FeatherWallet/comments/umgojt/feather_wallet_logo_redesign_feedback_wanted/*

The Monero Observer опубликовали очередной отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт здесь.

![11](/img/post/2022-05-12-the-monero-moon-42/11.png)  
*https://www.monero.observer/monero-dev-activity-report-week-18-2022/*

Интересно, как технология Monero работает на практике, если сравнивать с другими технологиями обеспечения приватности? Тогда прочитайте этот пост, опубликованный Джастином Эхренхофером (Justin Ehrenhofer). Следует отметить, что правое изображение взято из журнала, в то время как левое линейно. Очевидно, что ни одна технология не может сравниться с Monero.

![12](/img/post/2022-05-12-the-monero-moon-42/12.png)  

### _Прочие новости_

Управление по контролю за иностранными активами (OFAC), подразделение Министерства финансов США, занимающееся вопросами финансовой разведки и правоприменения, добавило в свой санкционный список криптовалютный миксер под названием Blender. Список также содержит множество адресов BTC и ETH.

![13](/img/post/2022-05-12-the-monero-moon-42/13.png)  
*https://home.treasury.gov/policy-issues/financial-sanctions/recent-actions/20220506*

Джастин Эхренхофер продемонстрировал, сколько денег придётся выделить правительству США, чтобы отследить платежи, совершаемые мигрантами.

![14](/img/post/2022-05-12-the-monero-moon-42/14.png)  

Нэм Сардар (Nam Sardar), основатель и гендиректор Neel Capital, недавно провела [подкаст](https://www.youtube.com/watch?v=VnNIqO9YTqE), в котором рассказала о Monero. Послушать подкаст можно ниже!

{{< youtube id="VnNIqO9YTqE" autoplay="false" >}}  

Также стоит посмотреть выступление с конференции Monerotopia, посвящённое развитию «бычьих тенденций Monero в свете инвестиционного портфолио в 2020-х».

{{< youtube id="4pLuOMTLdQE" autoplay="false" >}}  

### _Мероприятия_

The Monero Observer опубликовали подробный отчёт (с соответствующими ссылками) по встрече Рабочей группы сообщества Monero, состоявшейся 1 мая 2022 г. На встрече обсуждалось грядущее обновление сети, последние версии GUI/CLI, а также предложения, размещённые в системе CCS. К отчёту также прилагается «сырой» неотредактированный журнал чата. Всю информацию можно найти [здесь](https://www.monero.observer/meeting-log-summary-monero-community-workgroup-meeting-1-may-2022/).

[Есть информация](https://www.reddit.com/r/Monero/comments/uixoci/looking_for_a_speaker_at_mallorca_blockchain_days/), что Нэм Сардар, вероятно, посетит конференцию Bitcoin под названием [Mallorca Blockchain Days](https://mallorcablockchaindays.com), где выступит на тему Monero.

![15](/img/post/2022-05-12-the-monero-moon-42/15.png)  
*https://www.reddit.com/r/Monero/comments/uixoci/looking_for_a_speaker_at_mallorca_blockchain_days/*

[MoneroFox](https://www.reddit.com/r/Monero/comments/unaifx/monerorun2_tail_emission_day_june_8th_celebration/) предлагает сообществу Monero отпраздновать «День начала постэмисии» (8 июня), проведя Monerun2, и вывести все XMR с тех бирж, которые всё ещё поддерживают вывод Monero.

![16](/img/post/2022-05-12-the-monero-moon-42/16.png)  

8 июня в Нью-Йорке, Колорадо и Лас-Вегасе состоится Глобальное празднование (встреча по поводу) дня начала постэмиссии. Вы также можете отпраздновать окончание номинальной эмиссии Monero и начало постэмиссии со своим местным сообществом XMR! Вы даже можете организовать собственную встречу в своём городе! Всю дополнительную информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/).

![17](/img/post/2022-05-12-the-monero-moon-42/17.png)  
*https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/*

Следующая встреча разработчиков Monero пройдёт в субботу, 14 мая 2022 (17:00 UTC), на IRC-канале #monero-dev.

Очередная плановая встреча по проведению конференции MoneroKon 2022 также состоится в субботу, 14 мая 2022 года в 18:00 UTC, на IRC-канале #monero-events.

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Билеты на MoneroKon теперь можно приобрести [здесь](https://monerokon.com/products/monerokon2022), на веб-сайте MoneroKon.

![18](/img/post/2022-05-12-the-monero-moon-42/18.png)  
*https://monerokon.com/*

### _Биржи и предприниматели_

Казино Monero под названием MoKazino уже находится в стадии разработки. В [этом посте](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/304#note_16192) вы найдёте всю дополнительную информацию. Также вы можете посетить [веб-сайт](https://mokazino.net/) проекта.

![19](/img/post/2022-05-12-the-monero-moon-42/19.png)  
*https://mokazino.net/*

Если у вас возникнет желание, посетите обновлённый сайт MoneroPot.com. Они снизили размер реферального бонуса с 20 до 15% и добавили 5% к отчислениям в Общий фонд Monero, поскольку реферальная система использовалась не так активно.

![20](/img/post/2022-05-12-the-monero-moon-42/20.png)  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![21](/img/post/2022-05-12-the-monero-moon-42/21.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![22](/img/post/2022-05-12-the-monero-moon-42/22.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![23](/img/post/2022-05-12-the-monero-moon-42/23.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

Очередная неделя ознаменовалось падением цены Monero относительно как USD, так и BTC. В качестве причины инвесторы и трейдеры указывают на фиаско Terra Luna / UST и бычьи тенденции в целом, в силу которых люди предпочитают «не рисковать».

На момент написания бюллетеня пара XMR/USD приближалась к 200-недельному индикатору SMA. В данном случае возможно дальнейшее падение, если поддержка будет потеряна, а быки понадеются на отскок.

![24](/img/post/2022-05-12-the-monero-moon-42/24.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 119 879 XMR
- Общая рыночная капитализация Monero: 2 486 036.110 USD
- Позиция в рейтенге Coinmarketcap: 32
- Цена XMR/USD: ~135 USD
- Цена XMR/BTC: 0.00472 BTC
- Цена на LocalMonero.co: 166 USD
- Средний размер комиссии за проведение транзакции: 0.00011 XMR ($0.016)
- Хешрейт: 2.647 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![25](/img/post/2022-05-12-the-monero-moon-42/25.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![26](/img/post/2022-05-12-the-monero-moon-42/26.jpeg)  
*https://www.reddit.com/r/Monero/comments/uj15or/sound_%C9%B1oney_sidarta0/*

![27](/img/post/2022-05-12-the-monero-moon-42/27.png)  

![28](/img/post/2022-05-12-the-monero-moon-42/28.png)  
*https://twitter.com/JEhrenhofer/status/1524471709595750402*

![29](/img/post/2022-05-12-the-monero-moon-42/29.png)  
*https://www.reddit.com/r/monerochan/comments/mefc8e/sweet_lady_monerochan/*

![30](/img/post/2022-05-12-the-monero-moon-42/30.jpeg)  
*https://www.reddit.com/r/moonero/comments/q6e5fz/be_left_alone_use_monero/*

![31](/img/post/2022-05-12-the-monero-moon-42/31.jpeg)  

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 42)](https://www.themoneromoon.com/p/the-monero-moon-issue-42-e7e?s=r)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
