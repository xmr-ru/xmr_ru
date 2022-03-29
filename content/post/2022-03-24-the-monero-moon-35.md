---
title: "The Monero Moon (выпуск 35)"
date: "2022-03-24"
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

Следующая версия GUI	-кошелька Monero (который также можно использовать для майнинга) будет иметь встроенную поддержку P2Pool! Дополнительную информацию можно найти по [этой ссылке](https://github.com/monero-project/monero-gui/pull/3829).

![01](/img/post/2022-03-24-the-monero-moon-35/01.png)  
*https://github.com/monero-project/monero-gui/pull/3829*

[Monero Ecosystem объявляет](https://www.reddit.com/r/Monero/comments/tjn1zh/were_mature_moneropython_10_has_been_released/) о выпуске версии 1.0 monero-python, всеобъемлющей библиотеки Python для Monero. После трёхмесячного отсутствия сообщений об ошибках было принято решение опубликовать данную версию.

![02](/img/post/2022-03-24-the-monero-moon-35/02.png)  
*https://github.com/monero-ecosystem/monero-python*

mjxmr [опубликовал результаты оценки производительности своего инструмента](https://www.reddit.com/r/Monero/comments/tl5w1b/tsqsims_benchmark_new_tool_designed_for_monero/) для быстрого моделирования временных рядов (TSQSIM). TSQSIM был написан специально для Исследовательской лаборатории Monero с целью обеспечения возможности прогнозирования количества транзакций в ближайшем будущем. Результаты свидетельствуют об ускорении почти на два порядка величины. Вы можете узнать о  TSQSIM по [этой](https://github.com/mj-xmr/tsqsim) и [этой](https://www.reddit.com/r/Monero/comments/tl5w1b/tsqsims_benchmark_new_tool_designed_for_monero/) ссылке.

![03](/img/post/2022-03-24-the-monero-moon-35/03.png)  
*График, взятый из опубликованных mjxmr результатов тестирования TSQSIM*

Monero Observer рассказывает о работе разработчика Monero Rucknium, который поделился визуальным представлением распределения участников колец Monero по возрасту их появления в период с 2014 по 2022 год. В [этом посте](https://www.monero.observer/rucknium-shares-visualizations-monero-ring-member-age-distribution/#fn:2) довольно подробно описано то, над чем конкретно работает Rucknium.

![04](/img/post/2022-03-24-the-monero-moon-35/04.gif)  
*https://github.com/Rucknium/misc-research/blob/main/Monero-decoy-selection-empirical-evolution/images/Kernel-density-estimate-Monero-ring-member-age-monthly.gif*

hinto-janaiyo опубликовал версию v2.0.0 monero-toolchain, bash-скрипта, используемого для скачивания связанного с Monero программного обеспечения.

![05](/img/post/2022-03-24-the-monero-moon-35/05.png)  

Команда MyMonero ищет технически подкованных пользователей Monero, желающих принять участие в бета-тестировании их приложения MyMonero для iOS. Если вы готовы помочь им, свяжитесь с @tekkzbadger на Reddit. Также MyMonero создали Android-кошелёк, достойный того, чтобы вы попробовали им воспользоваться.

![06](/img/post/2022-03-24-the-monero-moon-35/06.png)  
*https://github.com/mymonero/mymonero-mobile*

noot [поделились](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/277#note_15490) новостями о продолжающейся работе по реализации возможности атомных свопов ETH-XMR. С полным вариантом отчёта можно ознакомиться [на Gitlab](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/277#note_15490).

![07](/img/post/2022-03-24-the-monero-moon-35/07.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/277#note_15490*

Давнишний контрибьютор проекта Monero Fluffy Pony [намекнул](https://twitter.com/fluffypony/status/1504430410415099914?s=20&t=tjr4PWJgERWqnfIAhYqUQw), что работает над тем, чтобы обеспечить возможность использования XMR в экосистеме DeFi.

![08](/img/post/2022-03-24-the-monero-moon-35/08.png)  

The Monero Observer опубликовали отчёт по деятельности разработчиков за 11 неделю 2022 года. Обязательно ознакомьтесь с этим материалом и оставайтесь в курсе всех новостей, связанных с разработкой Monero.

![09](/img/post/2022-03-24-the-monero-moon-35/09.png)  
*https://www.monero.observer/monero-dev-activity-report-week-11-2022/*

Интересно, какой объём информации становится публичным при проведении транзакций Bitcoin или Monero? [schlyza](https://www.reddit.com/user/schlyza/) предлагает вашему вниманию инфографику, позволяющую сравнить данные транзакций Bitcoin и Monero. Обфускация данных транзакций Monero делает эту криптовалюту самой надёжной с точки зрения обеспечения приватности

![10](/img/post/2022-03-24-the-monero-moon-35/10.jpeg)  
*https://www.reddit.com/r/Monero/comments/tkp77t/tx_data_comparison/*

### _Прочие новости_

Seth for Privacy опубликовал на LocalMonero.co пост под названием «Сравнение технологии кольцевых подписей, используемой Monero, и технологии CoinJoin, используемой кошельками типа Wasabi» ([Monero’s Ring Signatures vs CoinJoin Like in Wasabi](https://localmonero.co/knowledge/ring-signatures-vs-coinjoin)), в котором, собственно, сравнил технологию CoinJoin с кольцевыми подписями, а также разъяснил, почему подход Monero обеспечивает более надёжную защиту от цензурирования, более высокий уровень приватности и создаёт меньше неудобств для пользователей.

![11](/img/post/2022-03-24-the-monero-moon-35/11.png)  
*https://localmonero.co/knowledge/ring-signatures-vs-coinjoin*

Джон Фосс создал в Twitter тред под названием «Приватность финансовых данных — не преступление: Bitcoin, Zcash и Monero» (Financial Privacy Is Not a Crime: Bitcoin, Zcash, and Monero). В ветке обсуждается, как возрастает важность приватности финансовой информации для общества по мере того, как мир становится всё менее стабильным и движется в направлении создания валют CBDC.

![12](/img/post/2022-03-24-the-monero-moon-35/12.png)  

Джастин Эхренхофер опубликовал статью «Не обеспечивая приватность данных, мы создаём системы, способствующие дискриминации» ([Without Privacy, We Are Creating Systems to Discriminate](https://medium.com/@JEhrenhofer/without-privacy-we-are-creating-systems-to-discriminate-807dfb1f35e6)), в которой говорится о долгой истории сегрегации в Соединённых Штатах, а также о том, какую значительную роль в этом играл доступ к финансовым  активам. Читателю предлагается задуматься о том, как приватные криптовалюты, такие как Monero, могут помочь избежать подобной ситуации в будущем.

![13](/img/post/2022-03-24-the-monero-moon-35/13.png)  
*https://medium.com/@JEhrenhofer/without-privacy-we-are-creating-systems-to-discriminate-807dfb1f35e6*

В связи с вышеупомянутой проблемой  Electronic Frontier Foundation также опубликовали статью «Как ICE незаконным способом получили доступ к огромному количеству финансовой информации Western Union» ([Here’s How ICE Illegally Obtained Bulk Financial Records from Western Union](https://www.eff.org/deeplinks/2022/03/heres-how-ice-illegally-obtained-bulk-financial-records-western-union)). В статье рассказывается, как Иммиграционная и таможенная служба США (ICE) использовала административные повестки для получения миллионов финансовых записей Western Union и Maxitransfers Corporation и как получение «финансовой и другой личной информации лиц, подвергшихся домашнему насилию, беженцев и активистов, борющихся за права человека, может подвергнуть их риску, в частности, учитывая тот факт, что TRAC обеспечивает тысячи правоохранительных организаций доступом к таким записям».

Как сообщает Bitcoin Magazine, «на прошлой неделе служба по работе с клиентами HubSpot подверглась взлому, в результате чего произошла утечка личной информации тысяч пользователей Bitcoin, после того как злоумышленник получил доступ к аккаунту одного из сотрудников и экспортировал данные с 30 порталов HubSpot». Это самая настоящая проблема, поскольку личная информация позволяет хакерам совершать атаки на владельцев значительных сумм в криптовалюте. «Зачастую хакеры берут или покупают похищенную информацию с целью хищения Bitcoin, прибегая к различным технологиям, начиная с проведения простых [фишинговых атак](https://cybersecurityguide.org/resources/phishing/) и заканчивая [более сложными мошенническими схемами](https://bitcoinmagazine.com/technical/ledger-hack-victim-scam-details)».

Monero Talk опубликовали новое видео, в котором Дуглас Туман берёт интервью у Брайана Б. Солстина, кандидата в сенаторы США, целью которого является окончательная легализация Bitcoin. В интервью Брайан объясняет, почему доверие центральным банкам всегда приводило к последующей утрате такого доверия и снижению ценности валюты. Видео можно посмотреть по [этой ссылке](https://youtu.be/4waW9tGdFkA) или ниже.

{{< youtube id="4waW9tGdFkA" autoplay="false" >}}  
*https://youtu.be/4waW9tGdFkA*

Lovera также разместил на YouTube видео для испаноговорящих пользователей под названием NOTICIAS sobre [#MONERO](https://www.youtube.com/hashtag/monero) 14/03/2022 al 21/03/2022. Видео можно посмотреть ниже.

{{< youtube id="lGQO3k_Mv8k" autoplay="false" >}}  
*https://youtu.be/lGQO3k_Mv8k*

[Люк Смит](https://www.youtube.com/channel/UC2eYFnH61tmytImy1mTYvhA) опубликовал на YouTube видео «Будущее Monero (с Люком Смитом и Кевином Вадом)» (The Future of Monero (Luke Smith and Kevin Wad)). Это довольно длинное видео, в котором обсуждается Monero, Bitcoin, способы их использования, будущее и многое другое.

{{< youtube id="31eI9UD83PY" autoplay="false" >}}  
*https://youtu.be/31eI9UD83PY*

[robot4000](https://www.reddit.com/user/robot4000/) поделился инфографикой, в которой сравнил Monero с золотом, Bitcoin и фиатной валютой.

![14](/img/post/2022-03-24-the-monero-moon-35/14.png)  
*https://medium.com/@JEhrenhofer/without-privacy-we-are-creating-systems-to-discriminate-807dfb1f35e6*

LocalMonero.co опубликовали [The Monero Standard №5](https://localmonero.co/the-monero-standard/weekly/5), еженедельный новостной бюллетень, в котором освещаются события, так или иначе связанные с Monero.

### _Мероприятия_

Встреча Monero Space пройдёт в субботу, 26 марта в 17:00 UTC на IRC-канале #monero-space. Будут обсуждаться существующие и будущие проекты, организуемые сообществом Monero.

7 апреля в Майями состоится мероприятие под названием [Monerotopia](https://monerotopia.com/), где выступит множество интересных докладчиков, среди которых будет даже [Crytp0 Bear](https://www.youtube.com/channel/UCWC1InTHly5Tg-7e5P_S5Rw). Для тех, кто не сможет присутствовать лично, Даг из Monero Talk совместно с группой [The Crypto Vigilante](https://www.youtube.com/channel/UCWC1InTHly5Tg-7e5P_S5Rw) готовит виртуальные билеты, которые обеспечат доступ к «живому» эфиру конференции. Посетите [веб-сайт Monerotopia](https://monerotopia.com/) и приобретите билет на одну из самых жарких конференций Monero!

![15](/img/post/2022-03-24-the-monero-moon-35/15.png)  
*https://monerotopia.com/*

9-10 апреля в Майями [Guns N’ Bitcoin](https://gunsnbitcoin.com/) проведут мероприятие под названием Freedom Tech Trade Show and Conference. В этом году будет добавлена тема Monero, а на конференции выступят представители сообщества Monero. Более подробную информацию можно найти [здесь](https://gunsnbitcoin.com/).

![16](/img/post/2022-03-24-the-monero-moon-35/16.png)  
*https://gunsnbitcoin.com/*

Очередная плановая встреча по проведению MoneroKon 2022 состоится в воскресенье, 27 марта 2022 года в 18:00 UTC на IRC-канале #monero-events. Помимо этого, вы узнаете больше о конференции [Monerokon](monerokon.com), которая пройдёт в Лиссабоне, Португалия, 18-19 июня 2022 в [Arroz Studios](https://arrozestudios.pt/), если посетите веб-сайт MoneroKon 2022. Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов.

![17](/img/post/2022-03-24-the-monero-moon-35/17.png)  
*https://monerokon.com/*

### _Биржи и предприниматели_

Хотите потратить несколько XMR, но не знаете, где это сделать? На официальном веб-сайте Monero  [GetMonero.org](https://www.getmonero.org/community/merchants/) вы найдёте ссылки на Cryptwerk.com и AcceptedHere.io, директории, в которых содержится список предпринимателей, принимающих XMR.

![18](/img/post/2022-03-24-the-monero-moon-35/18.png)  
*https://www.getmonero.org/community/merchants/*

Packet Point теперь принимает Monero за использование виртуального сервера, расположенного в Канаде.

![19](/img/post/2022-03-24-the-monero-moon-35/19.png)  
*https://packetpoint.ca/blog/monero-now-accepted-for-virtual-server-hosting/*

### _Краудфандинговая система сообщества (CCS)_

Открыто финансирование по запросу [koe](https://packetpoint.ca/blog/monero-now-accepted-for-virtual-server-hosting/), который будет работать над доказательством концепции кошелька Seraphis. Средства можно пожертвовать [здесь](https://ccs.getmonero.org/proposals/seraphis-wallet-poc.html).

Финансирование по предложению mjxmr по написанию кода во втором квартале 2022 (частичная занятость) практически завершено. Внести средства можно [здесь](https://ccs.getmonero.org/proposals/mj-part-time-2022-q2.html).

Предложение по финансированию The Monero Observer весной 2022 года одобрено, и сбор пожертвований начат. Финансово поддержать их работу можно по этой [ссылке](https://ccs.getmonero.org/proposals/escapethe3ra-monero-observer-maintenance-spring-2022.html).

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![20](/img/post/2022-03-24-the-monero-moon-35/20.png)  

The Monero Moon разместили в CCS [очередной запрос на финансирование следующих 18-ти выпусков](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/294). Если вам нравится читать The Monero Moon, пожалуйста, поддержите наше предложение, оставив свой комментарий. Наш предыдущий запрос в CCS был опубликован [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/blob/master/john-foss-the-monero-moon.md). Дополнительную информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/tkoned/feedback_requested_would_you_like_the_monero_moon/).

Haveno разместили запрос о финансировании разработки их пользовательского интерфейса и функций, работающих с клиентской стороны. Более подробно обо всём можно узнать в их предложении, размещённом [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/295) в CCS.

CryptoGrampy предложил выплатить премию за разработку узла GUI для Android. Подробнее об этом можно узнать [здесь](https://bounties.monero.social/posts/59/android-gui-monero-node).

[Winston](https://repo.getmonero.org/winstonsthiccbooty) также разместил в CCS запрос о финансировании разработки FOSS-приложения для Android под названием Whatnero, в котором будет собрана и в удобной форме представлена вся доступная информация о Monero, чтобы новичкам или экспертам было проще найти нужную им информацию. С предложением можно ознакомиться по [этой ссылке](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/293).

Дональд А. Ильязи внёс предложение по переводу приложений, веб-сайтов и прочих материалов на греческий язык. Соответствующее предложение размещено [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/296).

Lovera опубликовал в CSS новый [отчёт](https://www.reddit.com/r/Monero/comments/ti6be2/lovera_ccs_february_report_a_lot_of_spanish/) за февраль. В нём в первую очередь отражена работа по написанию испаноязычного контента Monero. Отчёт можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ti6be2/lovera_ccs_february_report_a_lot_of_spanish/).

### _Торговля и биржевые спекуляции_

Aromatic-Poet6166 заглянул на Reddit и поделился скриншотом, свидетельствующем о наличии 9 миллионов XMR на финансовом рынке XMR Kucoin. Означает ли это, что Kucoin владеет 50% всей денежной массы XMR? Маловероятно. Скорее всего, Kucoin занимаются чем-то вроде частичного резервирования (подобном тому, в чём обвинялись Binance), чтобы извлечь выгоду. С тем, что по этому поводу думает сообщество Monero, можно ознакомиться [здесь](https://www.reddit.com/r/Monero/comments/tiqgfk/9_million_xmr_spoted_in_kucoin/).

![21](/img/post/2022-03-24-the-monero-moon-35/21.jpeg)  
*https://www.reddit.com/r/Monero/comments/tiqgfk/9_million_xmr_spoted_in_kucoin/*

Команда The Monero Talk поделилась видео Monerotopia, в котором, помимо прочего, содержится анализ цены XMR, интервью с различными гостями и прочая новостная информация, связанная с Monero. Часть, посвящённая анализу цены, начинается с временной метки 9:38!

{{< youtube id="Z346haSjiTs" autoplay="false" >}}  

Mr Legend Crypto опубликовали видео с 6 прогнозами по изменению цены Monero (XMR) в 2022 году и анализом диаграммы Altseason 2022.

{{< youtube id="oyxNbdKcgpA" autoplay="false" >}}  

_**Показатели**_
- Общее количество Monero в обращении: 18 097 223 XMR
- Общая рыночная капитализация Monero: 3 577 091 088 USD
- Цена XMR/USD: 197 USD
- Цена XMR/BTC: 0,00458 BTC
- Цена на LocalMonero.co: 220 USD
- Средний размер комиссии за проведение транзакции: 0.00011 XMR ($0.02)
- Хешрейт: 2.969 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![22](/img/post/2022-03-24-the-monero-moon-35/22.jpeg)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![23](/img/post/2022-03-24-the-monero-moon-35/23.jpeg)  
*https://www.reddit.com/r/xmrtrader/comments/l75n3s/this_entire_gamestop_situation_has_shown_exactly/*

![24](/img/post/2022-03-24-the-monero-moon-35/24.jpeg)  
*https://www.reddit.com/r/Monero/comments/54g0du/my_wife_got_me_a_monero_birthday_cake/*

![25](/img/post/2022-03-24-the-monero-moon-35/25.jpeg)  
*https://imgur.com/a/acuwX*

![26](/img/post/2022-03-24-the-monero-moon-35/26.jpeg)  
*https://www.reddit.com/r/moonero/comments/l51d4r/quick_reminder_of_how_time_can_fly_me_getting/*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 35)](https://www.themoneromoon.com/p/the-monero-moon-issue-35?s=r)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
