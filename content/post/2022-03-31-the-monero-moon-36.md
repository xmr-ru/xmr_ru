---
title: "The Monero Moon (выпуск 36)"
date: "2022-03-31"
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

Встреча разработчиков Monero состоится в субботу, 2 апреля 2022 года в 17:00 UTC. Будет обсуждаться переход сети на версию v15 протокола. Встреча будет проводиться на IRC/Libera/Matrix каналах #monero-dev. Всю дополнительную информацию можно найти по этой [ссылке](https://github.com/monero-project/meta/issues/680).

![01](/img/post/2022-03-31-the-monero-moon-36/01.png)  
*https://github.com/monero-project/meta/issues/680*

Команда RINO, некастодиального кошелька, поддерживающего схему мультиподписи, объявила о том, что готова выплатить вознаграждение в размере 10 000 USD за реализацию надёжной схемы multisig в рамках грядущего хардфорка. Члены команды RINO разъяснили важность схемы multisig, обосновав своё мнение тем, что «рабочий вариант реализации схемы multisig критически важен для проектов, использующих механизмы условного депонирования денежных сумм у третьих лиц, таких как [Haveno](https://haveno.exchange/), а также для юридических лиц, которым требуется надёжное хранение средств: для больших компаний, инвестиционных фондов, финансовых институтов и  даже для организаций, поддерживающих совместно используемые кошельки в интересах сообщества». Помимо заявленного вознаграждения команда RINO выразила готовность поддержать тех разработчиков, которые согласятся на финансирование через систему CCS.

![02](/img/post/2022-03-31-the-monero-moon-36/02.png)  
*https://www.reddit.com/r/Monero/comments/tqj5r6/lets_fix_multisig_rino_offering_10000_completion/*

[Dangerous Freedom](https://repo.getmonero.org/dangerousfreedom) разместил [CCS предложение](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/298) по разработке инструментов Python и образовательных материалов, которые позволят контролировать уровень инфляции Monero. Потенциально такие материалы помогут всем разобраться в том, как работает Monero.

![03](/img/post/2022-03-31-the-monero-moon-36/03.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/298*

[CryptoGrampy](https://www.reddit.com/user/CryptoGrampy/) ищет пользователей Android, готовых заняться тестированием PocketNode, приложения, позволяющего создать полный или обрезанный узел на устройстве Android. Вы можете связаться с Grampy по [этой ссылке](https://www.reddit.com/r/Monero/comments/tqba4l/android_pocketnode_any_android_users_want_to/).

![04](/img/post/2022-03-31-the-monero-moon-36/04.png)  

SChernykh выпустил версию v1.9 P2Pool. Обязательно проведите соответствующее обновление, так как в новой версии была исправлена критическая ошибка, связанная с генерированием фиксированного шаблона блоков. В результате этой ошибки узел производил майнинг доли, которая не подтверждалась другими узлами, и эти узлы просто не признавали такую долю. Ошибка особо сказывалась на работе узлов с высоким хешрейтом, так как они добывали большое количество долей.

[mj](https://repo.getmonero.org/mj) предложил создать новый проект под названием [SolOptXMR – оптимальный солнечный майнинг XMR](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/299). Цель проекта состояла бы в разработке открытого программного обеспечения, позволяющего пользователям выгодно заниматься майнингом Monero с помощью солнечной энергии.

mj также опубликовал свой отчёт по разработке за март, в котором были отмечены сложности, связанные с финансированием работы сообществом.

[Проект ACK-J](https://github.com/MAGICGrants/Monero-Fund/issues/15), цель которого состоит в оценке поверхности атаки кольцевых подписей в рамках машинного и глубинного обучения, был успешно профинансирован Фондом Monero по выплате междисциплинарных академических грантов в криптовалютной сфере (MAGIC). Это первый проект, профинансированный фондом [MAGIC](https://magicgrants.org/funds/monero/monero_fund/), общественной благотворительной организацией, занимающейся выплатой стипендий студентам, интересующимся криптовалютами, а также поддержкой всевозможной публичной платёжной криптовалютной инфраструктуры. Дополнительную информацию, связанную с фондом MAGIC, можно найти [здесь](https://magicgrants.org/). Если вы хотите принять участие в работе фонда, обязательно свяжитесь с ними.

![05](/img/post/2022-03-31-the-monero-moon-36/05.png)  
*https://magicgrants.org/*

Cake Wallet и их кошелёк Monero.com теперь поддерживают все 10 TLD Unstoppable Domains, включая домены Ethereum и Polygon. Это означает, что вы теперь сможете без каких-либо затруднений отправлять и принимать различные криптовалюты при помощи одного домена. Соответствующее объявление от Cake Wallet можно найти [здесь](https://i.imgur.com/hE8AVwM.mp4).

![06](/img/post/2022-03-31-the-monero-moon-36/06.png)  

XMR2020 поделился диаграммой, в которой сравнивается размер необрезанного узла Monero с размером популярной видеоигры. Диаграмма наглядно демонстрирует, что блокчейн Monero вовсе не является слишком большим или раздутым, как считают некоторые, и что в реальности Monero является одной из нескольких монет, позволяющих без труда создать и запустить узел в домашних условиях.

![07](/img/post/2022-03-31-the-monero-moon-36/07.png)  
*https://www.reddit.com/r/Monero/comments/tnm7kk/monero_full_node_size_vs_aaa_video_game/*

[pcre](https://www.reddit.com/user/pcre/) также поделился [графиком](https://www.reddit.com/r/Monero/comments/tq9gmi/monero_transactions_2019_today_smoother/), отражающим количество транзакций Monero начиная с 2019 года. На графике видно, что 2022 год начался с падения этого количества с последующим восстановлением, а также, что восходящий тренд сохраняется, даже несмотря на наличие некоторых спадов.

![08](/img/post/2022-03-31-the-monero-moon-36/08.jpeg)  
*https://www.reddit.com/r/Monero/comments/tq9gmi/monero_transactions_2019_today_smoother/*

pcre также опубликовал график, демонстрирующий среднее количество транзакций, проводимых в неделю в 2021 году. Самое интересное заключается в том, что чуть большее количество транзакций проводится в начале рабочей недели.

![09](/img/post/2022-03-31-the-monero-moon-36/09.png)  
*https://www.reddit.com/r/Monero/comments/tqx6tc/median_transactions_per_weekday/*

[anthemscores](https://www.reddit.com/r/Monero/comments/tnqaqg/my_experience_adding_a_monero_checkout_to_my_site/) поделился опытом добавления расчётов в Monero на свой веб-сайт без интеграции каких-либо сторонних инструментов.  Если вам интересна эта информация, обязательно ознакомьтесь с соответствующим [руководством](https://www.reddit.com/r/Monero/comments/tnqaqg/my_experience_adding_a_monero_checkout_to_my_site/).

![10](/img/post/2022-03-31-the-monero-moon-36/10.png)  
*https://www.reddit.com/r/Monero/comments/tnqaqg/my_experience_adding_a_monero_checkout_to_my_site/*

[The Monero Observer](https://www.monero.observer/monero-dev-activity-report-week-12-2022/) опубликовали очередной отчёт по деятельности разработчиков Monero. С отчётом можно ознакомиться по этой [ссылке](https://www.monero.observer/monero-dev-activity-report-week-12-2022/).

![11](/img/post/2022-03-31-the-monero-moon-36/11.png)  
*https://www.monero.observer/monero-dev-activity-report-week-12-2022/*

### _Прочие новости_

Проповедник принципов Bitcoin Андреас Антонополус разместил на YouTube видео под названием «Почему следует пользоваться Monero в целях обеспечения приватности» ([Should You Use Monero for Privacy](https://www.youtube.com/watch?v=pC5vHoTX6fE)), в котором объясняет, почему при отсутствии необходимости в высокой ликвидности (с точки зрения долларов) и острой нужде в соблюдении приватности лучше пользоваться Monero.

{{< youtube id="pC5vHoTX6fE" autoplay="false" >}}  
*https://youtu.be/pC5vHoTX6fE*

Агентство Reuters опубликовало статью «Криптовселенная: помните ли вы то время, когда Bitcoin был анонимным?» ([Cryptoverse: Remember when bitcoin was 'anonymous'?](https://www.reuters.com/technology/cryptoverse-remember-when-bitcoin-was-anonymous-2022-03-22/)) В статье говорится о том, что такие приватные монеты, как Monero, снова растут в цене, что Bitcoin вовсе не является приватной монетой, а также о том, что действительно приватные монеты ожидает рост цены в будущем.

![12](/img/post/2022-03-31-the-monero-moon-36/12.png)  
*https://www.reuters.com/technology/cryptoverse-remember-when-bitcoin-was-anonymous-2022-03-22/*

Стало известно о появлении нового закона под названием «Электронная валюта и безопасность аппаратного обеспечения» (ECASH), согласно которому министр финансов США должен заняться вопросом разработки и выпуска электронной версии доллара США, ориентированной на обеспечение приватности и анонимности транзакций. Более подробную информацию можно найти по этой [ссылке](https://ecashact.us/).

![13](/img/post/2022-03-31-the-monero-moon-36/13.png)  
*https://ecashact.us/*

Monero Talk опубликовали новое интервью с Майклом Руисом, сторонником Bitcoin и пропонентом цифровых электронных валют. В интервью Майкл делится, «почему его заботит вопрос приватности, взаимозаменяемости и централизации Bitcoin». Майкл считает, что «цифровая электронная валюта может улучшить жизнь абсолютно каждого, причём так, как никогда не было до этого».

{{< youtube id="Y25T0R8DiN0" autoplay="false" >}}  
*https://youtu.be/Y25T0R8DiN0*

Seth For Privacy, сторонник Monero, недавно принял участие в Bitcoin-подкасте Стефана Ливера, где обсудил недостаточный уровень взаимозаменяемости Bitcoin.

![14](/img/post/2022-03-31-the-monero-moon-36/14.png)  

[BluWorm](https://www.reddit.com/r/Monero/comments/tnhxl1/fungibility_is_the_essence_money_always/) поделился инфографикой, позволяющей оценить уровень взаимозаменяемости Monero без каких-либо языковых барьеров. Его новый крутой сайт с графиками, связанными с Monero, можно найти [здесь](https://cypherpunk-2022.ghost.io/the-separation-of-state-and-money/).

![15](/img/post/2022-03-31-the-monero-moon-36/15.png)  
*https://www.reddit.com/r/Monero/comments/tnhxl1/fungibility_is_the_essence_money_always/*

schlyza также поделился инфографикой, демонстрирующей простоту использования и уровень приватности Monero в сравнении с Bitcoin.

![16](/img/post/2022-03-31-the-monero-moon-36/16.jpeg)  
*https://www.reddit.com/r/Monero/comments/tq2yke/this_is_why_private_by_default_is_awesome/*

Kivojo опубликовал еженедельный новостной бюллетень The Monero Standard №6! Вы можете найти его здесь и узнать самые последние новости Monero.

### _Мероприятия_

Встреча Monero Space пройдёт в субботу, 26 марта в 17:00 UTC на IRC-канале #monero-space. Будут обсуждаться существующие и будущие проекты, организуемые сообществом Monero.

7 апреля в Майями состоится мероприятие под названием [Monerotopia](https://monerotopia.com/), где выступит множество интересных докладчиков, среди которых будет даже [Crytp0 Bear](https://www.youtube.com/channel/UCWC1InTHly5Tg-7e5P_S5Rw). Для тех, кто не сможет присутствовать лично, Даг из Monero Talk совместно с группой [The Crypto Vigilante](https://www.youtube.com/channel/UCWC1InTHly5Tg-7e5P_S5Rw) готовит виртуальные билеты, которые обеспечат доступ к «живому» эфиру конференции. Посетите [веб-сайт Monerotopia](https://monerotopia.com/) и приобретите билет на одну из самых жарких конференций Monero!

![17](/img/post/2022-03-31-the-monero-moon-36/17.png)  
*https://monerotopia.com/*

9-10 апреля в Майями [Guns N’ Bitcoin](https://gunsnbitcoin.com/) проведут мероприятие под названием Freedom Tech Trade Show and Conference. В этом году будет добавлена тема Monero, а на конференции выступят представители сообщества Monero. Более подробную информацию можно найти [здесь](https://gunsnbitcoin.com/).

![18](/img/post/2022-03-31-the-monero-moon-36/18.png)  
*https://gunsnbitcoin.com/*

Очередная плановая встреча по проведению [MoneroKon 2022](monerokon.com) состоится в воскресенье, 3 апреля 2022 года в 17:00 UTC на IRC-канале #monero-events. Помимо этого, вы узнаете больше о конференции Monerokon, которая пройдёт в Лиссабоне, Португалия, 18-19 июня 2022 в [Arroz Studios](https://arrozestudios.pt), если посетите веб-сайт MoneroKon 2022. Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов.

![19](/img/post/2022-03-31-the-monero-moon-36/19.png)  
*https://monerokon.com/*

### _Биржи и предприниматели_

На прошлой неделе Coincards заработали в Monero столько же, сколько до этого им удалось заработать в Bitcoin ранее. Coincards — это сервис, позволяющий приобрести подарочные карты, а также предоплаченные чеки, которые принимаются сотнями ретейлеров, предлагающими свои товары за криптовалюту.

![20](/img/post/2022-03-31-the-monero-moon-36/20.png)  

Представители криптовалютной биржи ChangeNOW объявили, что теперь некастодиальный, не требующий ввода каких-либо личных данных кошелёк NOW поддерживает Monero.

![21](/img/post/2022-03-31-the-monero-moon-36/21.png)  

Ребята из Cake Wallet запускают новый стартап под названием BlockBuy. Целью BlockBuy станет обеспечение возможности покупки Monero с помощью кредитных и дебетовых карт к маю 2022 года. Blockbuy будет независимой от Cake и Monero.com компанией. Больше информации содержится в твите ниже.

![22](/img/post/2022-03-31-the-monero-moon-36/22.png)  

Хотите потратить несколько XMR, но не знаете, где это сделать? На официальном веб-сайте Monero  GetMonero.org вы найдёте ссылки на Cryptwerk.com и AcceptedHere.io, директории, в которых содержится список предпринимателей, принимающих XMR.

![23](/img/post/2022-03-31-the-monero-moon-36/23.png)  
*https://www.getmonero.org/community/merchants/*

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![24](/img/post/2022-03-31-the-monero-moon-36/24.png)  

The Monero Moon разместили в CCS [очередной запрос на финансирование следующих 18-ти выпусков](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/294). Если вам нравится читать The Monero Moon, пожалуйста, поддержите наше предложение, оставив свой комментарий. Наш предыдущий запрос в CCS был опубликован [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/blob/master/john-foss-the-monero-moon.md). Дополнительную информацию можно найти по этой [ссылке](https://www.reddit.com/r/Monero/comments/tkoned/feedback_requested_would_you_like_the_monero_moon/).

willk опубликовал в CCS предложение под названием «Пусть больше людей пользуются Monero, push-уведомления в Telegram, проведение небольших транзакций за секунды, приватное развёртывание Docker, обеспечение бесплатного сервиса API».

[mj](https://repo.getmonero.org/mj) предложил создать новый проект под названием [SolOptXMR – оптимальный солнечный майнинг XMR](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/299).

Как упоминалось выше, [Dangerous Freedom](https://repo.getmonero.org/dangerousfreedom) разместил в системе CCS [предложение по разработке инструментов Python и образовательных материалов](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/298), которые позволят контролировать уровень инфляции Monero.

Hinto Janaiyo разместил предложение по разработке [monero-bash](https://github.com/hinto-janaiyo/monero-bash), оболочки monero, написанной в bash для Linux. С предложением можно ознакомиться [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/297).

Haveno разместили запрос о финансировании разработки их пользовательского интерфейса и функций, работающих с клиентской стороны. Более подробно обо всём можно узнать в их предложении, опубликованном [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/295).

CryptoGrampy предложил выплатить премию за разработку узла GUI для Android. Подробнее об этом можно узнать [здесь](https://bounties.monero.social/posts/59/android-gui-monero-node).

[Winston](https://repo.getmonero.org/winstonsthiccbooty) также разместил в CCS запрос о финансировании разработки FOSS-приложения для Android под названием Whatnero, в котором будет собрана и в удобной форме представлена вся доступная информация о Monero, чтобы новичкам или экспертам было проще найти нужную им информацию. С предложением можно ознакомиться по этой [ссылке](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/293).

Дональд А. Ильязи внёс предложение по переводу приложений, веб-сайтов и прочих материалов на греческий язык. Соответствующее предложение размещено [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/296).

Lovera опубликовал в CSS новый [отчёт за февраль](https://www.reddit.com/r/Monero/comments/ti6be2/lovera_ccs_february_report_a_lot_of_spanish/). В нём в первую очередь отражена работа по написанию испаноязычного контента Monero. Отчёт можно найти по этой [ссылке](https://www.reddit.com/r/Monero/comments/ti6be2/lovera_ccs_february_report_a_lot_of_spanish/).

### _Торговля и биржевые спекуляции_

Monero невероятно укрепилась и стремится к четырёхзначным показателям. Если поближе взглянуть на ежемесячный график XMR/USD, становится очевидным уход от почти годичного нисходящего тренда.

![25](/img/post/2022-03-31-the-monero-moon-36/25.png)  

А если немного отдалить ежемесячный график, то мы получим паттерн «чашка с ручкой» с целевой ценой примерно 2500 USD до укрепления и дальнейшего роста.

![26](/img/post/2022-03-31-the-monero-moon-36/26.jpeg)  

_**Показатели**_
- Общее количество Monero в обращении: 18 100 556 XMR
- Общая рыночная капитализация Monero: 3 987 123 925 USD
- Цена XMR/USD: 219 USD
- Цена XMR/BTC: 0,00467 BTC
- Цена на LocalMonero.co: 242 USD
- Средний размер комиссии за проведение транзакции: 0.00013 XMR ($0.025)
- Хешрейт: 2.701 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![27](/img/post/2022-03-31-the-monero-moon-36/27.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![28](/img/post/2022-03-31-the-monero-moon-36/28.jpeg)  
*https://boards.4channel.org/biz/thread/47551411/xmr-monero-general*

![29](/img/post/2022-03-31-the-monero-moon-36/29.png)  
*https://boards.4channel.org/biz/thread/47551411/xmr-monero-general*

![30](/img/post/2022-03-31-the-monero-moon-36/30.jpeg)  
*https://boards.4channel.org/biz/thread/47551411/xmr-monero-general*

![31](/img/post/2022-03-31-the-monero-moon-36/31.jpeg)  
*https://i.redd.it/gs6nbb85ltp81.jpg*

![32](/img/post/2022-03-31-the-monero-moon-36/32.jpeg)  
*https://boards.4channel.org/biz/thread/47551411/xmr-monero-general*

![33](/img/post/2022-03-31-the-monero-moon-36/33.png)  
*https://boards.4channel.org/biz/thread/47551411/xmr-monero-general*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 36)](https://www.themoneromoon.com/p/the-monero-moon-issue-36)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
