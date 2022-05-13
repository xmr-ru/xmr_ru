---
title: "The Monero Moon (выпуск 41)"
date: "2022-05-05"
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

Сообщаем о выходе новой версии CLI и GUI кошельков Monero — 0.17.3.2 Oxygen Orion! Не забудьте обновить своё программное обеспечение. Это позволит вам в полной мере воспользоваться всеми новыми функциями, исправить существующие ошибки и повысить уровень безопасности. Помимо прочих обновлений, в новой версии реализованы предупреждение пользователей о возможности уплаты значительной комиссией, поддержка Ledger Nano S Plus, а также интегрирована экспериментальная поддержка майнинга в P2Pool. Скачать новое программное обеспечение и узнать о нём больше можно по [этой ссылке](https://www.getmonero.org/blog/) или [на официальном веб-сайте](https://www.getmonero.org/blog/) Monero.

![01](/img/post/2022-05-05-the-monero-moon-41/01.png)  
*https://www.getmonero.org/downloads/*

Постэмиссия Monero начнётся уже приблизительно через 30 дней, и в связи с этим в официальном аккаунте Monero в Twitter был размещён тред, в котором разъясняется, зачем Monero нужна постэмиссия, как она работает и что это означает для рядовых пользователей. Соответствующий твит приводится ниже.

![02](/img/post/2022-05-05-the-monero-moon-41/02.png)  

Также сообщаем о выходе новой версии [P2Pool v2.0](https://github.com/SChernykh/p2pool/releases/tag/v2.0), в которой уже реализована поддержка грядущего обновления сети Monero. Среди новых особенностей стоит упомянуть добавление сборки FreeBSD и блокировку одноранговых узлов с зависающим или запаздывающим monerod. Помимо прочего был исправлен ряд небольших ошибок.

![03](/img/post/2022-05-05-the-monero-moon-41/03.png)  
*https://github.com/SChernykh/p2pool/releases/tag/v2.0*

hinto-janaiyo опубликовал новую версию оболочки monero-bash v1.5, которую можно найти [здесь](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.5)!

![04](/img/post/2022-05-05-the-monero-moon-41/04.png)  
*https://github.com/hinto-janaiyo/monero-bash*

noot поделился новостями, связанными с его проектом по реализации атомных свопов ETH-XMR. Соответствующий материал можно найти по этой ссылке.

![05](/img/post/2022-05-05-the-monero-moon-41/05.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/277#note_16140*

На ресурсе XMRSwap.me появилось видео с проведением атомного свопа посредством мобильного устройства.

![06](/img/post/2022-05-05-the-monero-moon-41/06.png)  

ACK-J опубликовал апрельский отчёт о своей работе в рамках аудита безопасности и устойчивости кольцевой подписи к атакам с применением машинного/глубокого обучения. Ознакомиться с отчётом можно [здесь](https://github.com/MAGICGrants/Monero-Fund/issues/15).

![07](/img/post/2022-05-05-the-monero-moon-41/07.png)  
*https://github.com/MAGICGrants/Monero-Fund/issues/15*

Seth For Privacy сделал публичный запрос в отношении лицензирования кода Zcash и [успокоил всех тех, кто считает, что разработчики Monero пытаются перенести Monero на технологии Zcash](https://www.reddit.com/r/Monero/comments/uf2ewh/no_the_monero_devs_are_not_trying_to_migrate/). Seth заявляет, что целью его запросов являются все те, кто открыт и допускает использование самых передовых технологий в интересах Monero в будущем. Также он разместил в GitHub репозитории проекта Monero [предложение](https://github.com/monero-project/research-lab/issues/100) по созданию «места для сбора ссылок, информации и всего необходимого для построения не требующих доверия доказательств zk-SNARKs, которые можно было бы использовать в качестве компонента протокола Monero в будущем».

![08](/img/post/2022-05-05-the-monero-moon-41/08.png)  
*https://github.com/monero-project/research-lab/issues/100*

Кто-то недавно умудрился заплатить 19 XMR за проведение транзакции с помощью удаленного узла и GUI-кошелька Monero. В простом режиме GUI-кошелёк Monero выбирает случайный удалённый узел, который может оказаться вредоносным и значительно увеличить размер комиссии. После недавнего обновления GUI-кошелька пользователи получают предупреждение, если размер транзакции оказывается значительным. И всё же дважды проверяйте сумму комиссии, каким бы кошельком Monero вы не пользовались.

![09](/img/post/2022-05-05-the-monero-moon-41/09.png)  
*https://github.com/monero-project/monero/issues/8298*

Теперь возможность переплаты по комиссии за проведение транзакции при использовании удалённого узла стала одной из причин, по которой рекомендуется создавать собственные узлы Monero. Если вам интересно, что означает создание и запуск собственного узла, зачем это нужно в принципе  и как это сделать, обязательно прочитайте этот [пост](https://sethforprivacy.com/guides/), опубликованный Seth for Privacy, или посмотрите это новое видео из серии Monero Guides.

{{< youtube id="XonyYxjjfcg" autoplay="false" >}}  

Помимо этого стоит посмотреть это [видео](https://www.youtube.com/watch?v=OviYhLZ02qg) от [Luigi Tech](https://www.youtube.com/watch?v=OviYhLZ02qg). Из него вы узнаете, как настроить узел через Tor с помощью Docker Compose.

{{< youtube id="OviYhLZ02qg" autoplay="false" >}}  

![10](/img/post/2022-05-05-the-monero-moon-41/10.png)  
*Любой пользователь будет только рад увидеть синхронизированный полный узел! :-)*
https://www.reddit.com/r/Monero/comments/uewy19/finally_full_local_node/

У вас есть лэптоп, который валяется где-то в доме без дела? Воспользуйтесь им, чтобы настроить и запустить полный узел, как это сделал Gingeropolous!

![11](/img/post/2022-05-05-the-monero-moon-41/11.png)  

[HefMcHefHef](https://www.reddit.com/r/MoneroMining/comments/ues8o8/my_24x_mac_mini_rack_is_finished/) продемонстрировал свою майнинговую ферму на базе 24-х Mac Mini. Со слов HefMcHefHef это «довольно простая сборка: 24 CPU M1 в самой дешёвой конфигурации. 500W потребляемой мощности вместе с коммутатором. Выдаёт примерно 57-60 kh/s».

![12](/img/post/2022-05-05-the-monero-moon-41/12.png)  
*https://www.reddit.com/r/MoneroMining/comments/ues8o8/my_24x_mac_mini_rack_is_finished/*

_xd22 предложил обновить майнеры Monero с помощью приложения Telegram. Всю дополнительную информацию можно найти в [этом посте](https://www.reddit.com/r/Monero/comments/ufbgf7/update_miners_i_made_you_bot_you_cant_say_no_to/).

![13](/img/post/2022-05-05-the-monero-moon-41/13.png)  
*https://www.reddit.com/r/Monero/comments/ufbgf7/update_miners_i_made_you_bot_you_cant_say_no_to/*

Теперь у пользователей появилась возможность майнинга Monero в пуле с автоматическим обменом [Zergpool.com](https://zergpool.com/). Размер комиссии составляет 0,5%. Более подробную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/ugko5v/xmr_mining_at_zergpoolcom/).

[NOWNodes](https://nownodes.io/nodes/monero-xmr), BaaS-решение (Blockchain-as-a-Service), теперь поддерживает Monero. Если это то, чего не хватало вашему бизнесу, или вы не можете самостоятельно запустить свой узел, вы найдёте их по [этой ссылке](https://nownodes.io/nodes/monero-xmr).

В рамках обновления сети Monero, которое произойдёт в июле, будет реализована функция под названием «теги просмотра» (View Tags), которая позволит сократить время синхронизации кошельков на 40%. Командой Cake Wallet была опубликована инфографика, наглядно демонстрирующая, какую выгоду получат от них пользователи мобильных устройств. Но даже несмотря на это, если ваш кошелёк настроится на удалённый узел, существует вероятность, что теги просмотра не позволят сократить время. [j-berman](https://github.com/j-berman) поделился великолепным обзором того, чего ожидать (и чего не ожидать) от тегов просмотра. С обзором можно ознакомиться [здесь](https://www.reddit.com/r/Monero/comments/udndu4/what_to_expect_and_what_not_to_expect_from_the/).

![14](/img/post/2022-05-05-the-monero-moon-41/14.png)  
*https://www.reddit.com/r/Monero/comments/ugx4m5/how_much_will_phones_benefit_from_view_tags_cake/*

Наконец-то начиная с прошлого месяца Monero Talk на своём YouTube-канале начали публиковать свои записи с конференции Monerotopia. Так вы можете теперь посмотреть выступление Франсиско Кабаньаса (Francisco Cabañas), также известного как ArticMine, по вопросу масштабирования Monero.

{{< youtube id="9RJ5HDmuucY" autoplay="false" >}}  

[dsmlegend](https://www.reddit.com/r/Monero/comments/ugh7ja/savandras_animated_videos_ccs_update_feedback/) ожидает реакции сообщества Monero на техническое содержание созданных им коммерческих видео, посвящённых Monero. Если вы желаете помочь, [свяжитесь с ним](https://www.reddit.com/r/Monero/comments/ugh7ja/savandras_animated_videos_ccs_update_feedback/).

[The Monero Observer](https://www.monero.observer/) опубликовали очередной отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://www.monero.observer/monero-dev-activity-report-week-17-2022/).

![15](/img/post/2022-05-05-the-monero-moon-41/15.png)  

### _Прочие новости_

Представители децентрализованной биржи Haveno заявили, что не станут осуществлять поддержку Zcash (в виде пары XMR-ZEC) при запуске платформы, как об этом было объявлено вначале. Тогда это вызвало самую неблагоприятную реакцию со стороны некоторых членов сообщества Monero. Полный текст последнего заявления можно найти [здесь](https://haveno.exchange/2022/04/29/haveno-zcash.html), на веб-сайте биржи.

![16](/img/post/2022-05-05-the-monero-moon-41/16.png)  
*https://haveno.exchange/2022/04/29/haveno-zcash.html*

На криптовалютном You-Tube-канале Coin Bureau, насчитывающем более 2 миллионов подписчиков, появилось великолепное [видео](https://www.youtube.com/watch?v=7-aTYyEVlNk), полностью посвящённое Monero и перспективам монеты в 2022 году. Обязательно посмотрите его и поделитесь со своими друзьями. Весь материал изложен довольно подробно и понятным новичку языком.

{{< youtube id="7-aTYyEVlNk" autoplay="false" >}}  

Команда Monero Talk стабильно продолжает выкладывать видео с конференции Mopnerotopia, которая проводилась в прошлом месяце. Все уже опубликованные видео можно найти [здесь](https://www.youtube.com/c/MoneroTalk/videos). Среди прочих Monero Talk поделились [новым видео](https://www.youtube.com/watch?v=dMrScvkvKDo), в котором Даг и Эдвард РА (Edward RA), член законодательного собрания штата Нью-Йорк, обсуждают проблемы майнинга с применением алгоритма доказательства работы.

{{< youtube id="Inm4uPTqUtc" autoplay="false" >}}  

Опубликован 118-й выпуск Revuo Monero. Revuo Monero — это еженедельный новостной бюллетень, посвящённый Monero. Новый выпуск можно найти по [этой ссылке](https://revuo-xmr.com/issue-118.html).

The Monero Observer опубликовали ежемесячную подборку новостей Monero под названием «Monero Observer Blitz #9 – апрель 2022».

![17](/img/post/2022-05-05-the-monero-moon-41/17.png)  
*https://www.monero.observer/monero-observer-blitz-april-2022/*

Владельцы Bitcoin сообщают о получении предупреждений со стороны криптовалютных бирж после вывода и отправки своих DTC на адреса, защищённые с помощью технологии CoinJoin. Стоит задуматься, с какой такой целью биржи занимаются анализом блокчейна уже после того, как пользователи выводят свои средства.

![18](/img/post/2022-05-05-the-monero-moon-41/18.png)  

Европейский центральный банк опубликовал отчёт под заголовком «Отчёт Евросистемы по публичным слушаниям по вопросу цифрового евро» ([Eurosystem report on the public consultation on a digital euro](https://www.ecb.europa.eu/pub/pdf/other/Eurosystem_report_on_the_public_consultation_on_a_digital_euro~539fa8cd8d.en.pdf)). Как следует из отчёта, для большинства респондентов приватность цифрового евро является самым важным из свойств валюты.

![19](/img/post/2022-05-05-the-monero-moon-41/19.png)  
*https://www.ecb.europa.eu/pub/pdf/other/Eurosystem_report_on_the_public_consultation_on_a_digital_euro~539fa8cd8d.en.pdf*

Легендарный инвестор Рэй Далио (Ray Dalio) признаёт недостатки Bitcoin, а также необходимость и ценность возможности совершения транзакций с нулевым разглашением информации.

{{< youtube id="1Jyz34BJN_c" autoplay="false" >}}  

Хотите поразвлечься? Почитайте [анализ](https://cryptofireside.com/is-bitcoin-a-shitcoin-5b7e54df7581) недавних дебатов между сторонником Monero Рафаэлем Лаверде (Rafael LaVerde) и пропонентом Bitcoin Тоном Вайсом (Tone Vays).

Наконец, если у вас есть вопросы, связанные с Monero, присоединяйтесь к проводимому по понедельникам сеансу вопросов и ответов под названием «MAAM — всё, что вы хотели знать о Monero» ([MAAM – Monero Ask Anything Monday](https://www.reddit.com/r/Monero/comments/uglikv/maam_monero_ask_anything_monday_may_02_2022/)). Спрашивайте обо всём, что вас интересует в Monero. Задавайте даже самые тупые вопросы, которые просто боялись задать до этого.

### _Мероприятия_

Сегодня (05.05.2022) в 18:00 в Кейптауне, Южная Африка, в баре Dark Horse состоится Встреча сообщества Monero. Всю дополнительную информацию можно найти по [этой ссылке](https://www.meetup.com/cape-town-privacy-meetup-group/events/285516314/?_xtd=gqFyqTIxNzM0ODMxNaFwo2FwaQ&from=ref).

![20](/img/post/2022-05-05-the-monero-moon-41/20.png)  
*https://www.meetup.com/cape-town-privacy-meetup-group/events/285516314/?_xtd=gqFyqTIxNzM0ODMxNaFwo2FwaQ&from=ref*

Следующая встреча разработчиков Monero пройдёт в субботу, 7 мая 2022 (17:00 UTC) на IRC-канале #monero-dev.

Очередная плановая встреча по проведению конференции MoneroKon 2022 состоится в субботу, 7 мая 2022 года в 18:00 UTC на IRC-канале #monero-events.

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Билеты на MoneroKon теперь можно приобрести [здесь](https://monerokon.com/products/monerokon2022), на веб-сайте MoneroKon.

![21](/img/post/2022-05-05-the-monero-moon-41/21.png)  
*https://monerokon.com/*

### _Биржи и предприниматели_

Команда Haveno ждёт от сообщества Monero предложений по тем активам, которые, по мнению пользователей, должна поддерживать биржа. Свой отзыв можно оставить, перейдя по твиту, который приводится ниже, и дальше по соответствующим ссылкам.

![22](/img/post/2022-05-05-the-monero-moon-41/22.png)  

Coincards сообщают, что в апреле Monero стала одной из самых популярных криптовалют, используемых для оплаты на Coincards, и однозначно самой популярной в США.

![23](/img/post/2022-05-05-the-monero-moon-41/23.png)  

VPN-сервис Mullvad теперь принимает оплату в XMR! Однако помните о том, что при оплате услуг, предоставляемых сервисом, в Monero возмещение средств не поддерживается. Не пользуйтесь одноразовыми адресами. При этом обработка платежа может занять до 30 минут.

![24](/img/post/2022-05-05-the-monero-moon-41/24.png)  
*https://mullvad.net/en/blog/2022/5/3/we-now-accept-monero/*

PhotoPrism, приложение для работы с фото в децентрализованной сети на базе искусственного интеллекта, теперь принимает пожертвования в Monero. Чтобы узнать больше, посетите [веб-сайт](https://photoprism.app/) проекта.

Shopinbit предлагают скидку в 3% плюс три бесплатные доставки в пределах ЕС при покупке телефона с приватной ОС Lineage за Monero. С предложением можно ознакомиться по [этой ссылке](https://shopinbit.com/electronics/tablets-and-smartphones/lineageos-compatible/).

После некоторой путаницы [Monero.com app](https://www.monero.com/) снова можно скачать в Google Play!

![25](/img/post/2022-05-05-the-monero-moon-41/25.png)  
*https://play.google.com/store/apps/details?id=com.monero.app*

Хотите светильник Monero? Свяжитесь с [matt_woodiwiss890](https://www.reddit.com/r/Monero/comments/uiadxx/hi_all_still_making_my_lights_if_anyone_is/), и он сделает вам такой!

![26](/img/post/2022-05-05-the-monero-moon-41/26.png)  
*https://www.reddit.com/r/Monero/comments/uiadxx/hi_all_still_making_my_lights_if_anyone_is/*

### _Краудфандинговая система сообщества (CCS)_

Сообщаем о запуске новой краудфандинговой платформы Monero под названием XMRStarter. Цель платформы состоит в том, чтобы помочь пользователям в организации кампаний для финансирования их проектов, подобно тому как это происходит в случае с официальной системой Monero CCS. Узнайте больше, перейдя по [этой ссылке](https://xmrstarter.com/).

![27](/img/post/2022-05-05-the-monero-moon-41/27.png)  
*https://xmrstarter.com/*

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![28](/img/post/2022-05-05-the-monero-moon-41/28.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![29](/img/post/2022-05-05-the-monero-moon-41/29.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![30](/img/post/2022-05-05-the-monero-moon-41/30.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

Lion247 заявляет, что «цена XMR/USD отскочила от предшествующей зоны сопротивления, поэтому до следующей такой зоны можно ожидать [активности быков](https://www.tradingview.com/ideas/bullish/)».

![31](/img/post/2022-05-05-the-monero-moon-41/31.png)  
https://www.tradingview.com/chart/XMRUSD/lkrUdYwh-Bullish/

Monero продемонстрировала обратный паттерн «голова и плечи» в паре XMR/USD.

![32](/img/post/2022-05-05-the-monero-moon-41/32.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 116 778 XMR
- Общая рыночная капитализация Monero: 4 127 990.922 USD
- Позиция в рейтенге Coinmarketcap: 35
- Цена XMR/USD: 228 USD
- Цена XMR/BTC: 0.00577 BTC
- Цена на LocalMonero.co: 253 USD
- Средний размер комиссии за проведение транзакции: 0.000079 XMR ($0.018)
- Хешрейт: 2.864 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![33](/img/post/2022-05-05-the-monero-moon-41/33.png)  
_https://minexmr.com/pools.html_

### _Для развлечения_

rbrunner7 опубликовал очередной фанфик про Monero. Все его работы можно прочитать [здесь](https://rbrunner7.github.io/numerator.html).

![34](/img/post/2022-05-05-the-monero-moon-41/34.png)  
*https://www.reddit.com/r/Monero/comments/ugseuh/numerator_a_monero_fiction_short_story/*

![35](/img/post/2022-05-05-the-monero-moon-41/35.png)  
*https://www.reddit.com/r/Monero/comments/uicl5j/monero_license_plate/*

![36](/img/post/2022-05-05-the-monero-moon-41/36.png)  
*https://twitter.com/DontTraceMeBruh/status/1518171946571210753/photo/1*

![37](/img/post/2022-05-05-the-monero-moon-41/37.png)  
*https://www.reddit.com/r/monerochan/comments/r6j97r/monerochan_upset_after_another_boating_accident/*

![38](/img/post/2022-05-05-the-monero-moon-41/38.png)  
*https://www.reddit.com/user/RoyalMayonnaise/posts/?sort=top*

![39](/img/post/2022-05-05-the-monero-moon-41/39.png)  
*https://www.reddit.com/r/monerochan/comments/twou2g/the_world_needs_more_chomnky_brown_monerochan/*



---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 41)](https://www.themoneromoon.com/p/the-monero-moon-issue-41)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
