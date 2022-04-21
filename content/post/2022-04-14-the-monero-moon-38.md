---
title: "The Monero Moon (выпуск 38)"
date: "2022-04-14"
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

_К сожалению, вероятно, на данный момент времени это последний выпуск The Monero Moon, поскольку предложение The Monero Moon о финансировании в системе CCS не было одобрено. Спасибо всем тем, кто поддерживал и вносил пожертвования для The Monero Moon. Дополнительную информацию в этом отношении можно найти здесь. А пока ещё есть время насладиться этим выпуском и бокалом «Бароло»!_

### _Разработка, новые версии и технологии_

Сообщаем о выходе версии [Monero-Bash v1.0.0](https://github.com/hinto-janaiyo/monero-bash). Monero-Bash — это оболочка/менеджер Linux для monerod, monero-wallet-cli, xmrig и p2pool, написанная на Bash. Как видно на видео, monero-bash можно использовать для загрузки, настройки и запуска майнинга на P2Pool менее чем за две минуты.

![01](/img/post/2022-04-14-the-monero-moon-38/01.png)  
*https://www.reddit.com/r/Monero/comments/u0s8z5/monerobash_v100_released/*

eversinc33 написал на Nim экспериментальный вариант реализации клиента для RPC-сервера кошелька [Monero](https://www.getmonero.org/). Подробности можно узнать [здесь](https://github.com/eversinc33/nim-monero-rpc).

![02](/img/post/2022-04-14-the-monero-moon-38/02.png)  
*https://github.com/eversinc33/nim-monero-rpc*

unyeildinggrace создал [Monerod-Proxy](https://github.com/unyieldinggrace/monerod-proxy). Monerod-Proxy — это небольшой HTTP прокси-сервер, предназначенный для развёртывания перед реальным узлом Monerod. Ваш кошелёк (или другое приложение, которому требуется узел) может обмениваться данными с прокси так же, как если бы обмен происходил напрямую с узлом, но уже с добавлением некоторых полезных дополнительных функций. Это, возможно, будет удобно, если вы захотите принять XMR в качестве оплаты, будучи предпринимателем!

![03](/img/post/2022-04-14-the-monero-moon-38/03.png)  
*https://github.com/unyieldinggrace/monerod-proxy*

Cake Wallet обновили свой кошелёк Monero, Monero.com v1.0.5. Обновление включает в себя ряд изменений в дизайне, делает обмен проще, а также содержит библиотеку Monero lib версии 0.17.3! В [этом посте](https://www.reddit.com/r/Monero/comments/u04hcd/update_monerocom_105_new_home_screen_design_yats/) вы найдёте всесторонний обзор обновления!

![04](/img/post/2022-04-14-the-monero-moon-38/04.png)  
*https://monero.com/*

Недавно DarkFi Squad предложили Monero свою помощь в переходе от кольцевых подписей к не требующим доверительных настроек zk-SNARKS в будущем.

![05](/img/post/2022-04-14-the-monero-moon-38/05.png)  

Силла Бример (Csilla Brimer) поделилась изображением концептуального аппаратного кошелька Monero.

![06](/img/post/2022-04-14-the-monero-moon-38/06.png)  

userpc123 [посоветовал избегать](https://www.reddit.com/r/MoneroMining/comments/u00hov/the_minergate_mining_pool_became_a_scam_no_longer/) пула MinerGate при майнинге, поскольку сам не смог получить свои XMR. Пул MinerGate давно не вызывает доверия. Поэтому если вы занимаетесь майнингом, то [здесь](https://www.getmonero.org/get-started/mining/) вы найдёте лучшие варианты.

![07](/img/post/2022-04-14-the-monero-moon-38/07.png)  
*https://www.getmonero.org/get-started/mining/*

Настоятельно рекомендуем создать и использовать собственный узел или заняться майнингом, так как это способствует защите сети. Также возможен соло-майнинг с помощью официального GUI-кошелька Monero, который можно скачать [здесь](https://www.getmonero.org/downloads/), или, что ещё лучше, пользователи могут заниматься майнингом в пуле, присоединившись к децентрализованному и не требующему разрешений пулу [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html).

Специалист по криптовалютам и разработчик Bulletproofs Бенедикт Бюнц (Benedikt Bünz) отметил, что в описании Bulletproofs Фиата Шамира (Fiat-Shamir) обнаружена уязвимость (в нём не хватает очевидного хеширования заявления), однако это никак не сказалось на Monero в целом.

![08](/img/post/2022-04-14-the-monero-moon-38/08.png)  

[The Monero Observer](https://www.monero.observer/) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://www.monero.observer/monero-dev-activity-report-week-14-2022/).

![09](/img/post/2022-04-14-the-monero-moon-38/09.png)  
*https://www.monero.observer/monero-dev-activity-report-week-14-2022/*

Хотите присоединиться к проекту Monero, но не знаете, каким может быть ваш вклад или с чего начать? Загляните на сайт [The Monero Ecosystem](https://moneroecosystem.org/). Его разработка заняла много времени, но теперь мы имеем «коллекцию проектов, поддерживаемых членами сообщества Monero... Основная цель состоит в том, чтобы собрать все активные и высококачественные проекты Monero в рамках одной экосистемы, в которой было бы легко ориентироваться и которую было бы просто найти».

![10](/img/post/2022-04-14-the-monero-moon-38/10.png)  
*https://moneroecosystem.org*

### _Прочие новости_

18 апреля Monero празднует свой 8-й день рождения! И несмотря на то, что это самое подходящее время для того, чтобы открыть бутылочку «Бароло» и отметить событие, члены сообщества Monero используют эту дату, чтобы побудить других отозвать свои XMR с бирж в целях повышения уровня приватности и ограничения количества XMR, которыми владеют биржи. Это позволит пресечь любые возможные махинации, связанные с частичным резервированием, которые совершаются нечестными биржами. В Telegram существует даже [группа членов сообщества Monero](https://t.me/moneroexchangerun), поддерживающих это движение. Представители сообщества Monero [утверждают](https://www.reddit.com/r/xmrtrader/comments/tzn6hj/xmr_withdrawals_disabled/), что нечестные биржи регулярно переводят кошельки XMR или функцию вывода средств в режим «обслуживания», а это признак того, что биржи на самом деле не имеют столько XMR, сколько, как они утверждают, у них есть на самом деле.

![11](/img/post/2022-04-14-the-monero-moon-38/11.png)  
*https://t.me/moneroexchangerun*

Конференция Monerotopia увенчалась невероятным успехом! monerodl опубликовал видео и слайды с мероприятия, которые вы можете посмотреть, если вы не смогли присутствовать там лично. Каждое из опубликованных видео стоит того, чтобы его посмотреть, поэтому счастливой вам Пасхи, и смотрите Monerotopia!

![12](/img/post/2022-04-14-the-monero-moon-38/12.png)  
*https://monerodl.com/monerotopia/*

[Здесь](https://www.youtube.com/watch?v=5waLjVadYug) вы также можете посмотреть интервью с гостями Monerotopia, взятые командой Monero Talk после конференции.

{{< youtube id="5waLjVadYug" autoplay="false" >}}  

Либертарианская партия Майами-Дейд в своём блоге сообщила о том, что Аллан Теппер (Allan Tépper) из TecnoTur и радио [CapicúaFM](https://tecnotur.us/capicuafm/) стали официальными СМИ на первой в истории конференции MoneroTopia, и рассмотрела выводы, сделанные Алланом по итогам. Более подробно об этом можно прочитать [здесь](https://lpmiamidade.org/2022/04/12/two-crypto-currency-conferences-in-miami-beach/).

![13](/img/post/2022-04-14-the-monero-moon-38/13.png)  
*https://lpmiamidade.org/2022/04/12/two-crypto-currency-conferences-in-miami-beach/*

О Monero говорится в [эпизоде крипто-новостей от Coin Bureau](https://www.youtube.com/watch?v=llpjvqjflVc&t=1137s), создателя крипто-контента на YouTube, насчитывающего более 2 миллионов подписчиков. Видео можно посмотреть ниже. Monero упоминается на восемнадцатой минуте (18:57).

{{< youtube id="llpjvqjflVc" autoplay="false" >}}  

[Privacy X](https://www.youtube.com/channel/UC8JrOitrLRmBTYty6kzIFFQ) опубликовал видео, в котором обсуждается необходимость приватности в нашем развивающемся мире и довольно позитивно говорится о Monero. Видео можно найти [здесь](https://youtu.be/5Tsv2goiQe4?t=351). О Monero говорится примерно начиная с 5:51.

{{< youtube id="5Tsv2goiQe4" autoplay="false" >}}  

[LoveraTV](https://www.youtube.com/channel/UCqNAqtUtyGmj3uFrFXhSyzwhttps:/www.youtube.com/channel/UC8JrOitrLRmBTYty6kzIFFQ) поделился новым видео с последними еженедельными новостями Monero на испанском языке. Смотрите видео ниже.

{{< youtube id="3o_2suqpGvs" autoplay="false" >}}  

Опубликован очередной выпуск The Monero Standard. Ознакомиться с ним можно [здесь](https://localmonero.co/the-monero-standard/weekly/8).

[germaphober](https://www.reddit.com/user/germaphober/) поделился интересным смонтированным видео изречений телеведущего ток-шоу Джона Оливера (John Oliver), на протяжении многих лет меняющего своё мнение в отношении технологий обеспечения приватности. Это изумительное видео можно найти по [данной ссылке](https://www.reddit.com/r/Monero/comments/u2flle/john_olivers_hypocritical_views_on_monero_and/).

![14](/img/post/2022-04-14-the-monero-moon-38/14.png)  
*https://www.reddit.com/r/Monero/comments/u2flle/john_olivers_hypocritical_views_on_monero_and/*

В недавнем интервью популярный макроинвестор Рауль Пал (Raoul Pal) упоминает Monero как очевидный выбор тех, кто заботится о собственной приватности. Короткий отрывок видео можно посмотреть [здесь](https://www.reddit.com/r/ethereum/comments/u247cv/raoul_pal_talks_about_ethereum_solana_and_monero/?utm_source=share&utm_medium=web2x&context=3). О Monero говорится уже на первой минуте (1:07).

![15](/img/post/2022-04-14-the-monero-moon-38/15.png)  
*https://www.reddit.com/r/ethereum/comments/u247cv/raoul_pal_talks_about_ethereum_solana_and_monero/?utm_source=share&utm_medium=web2x&context=3*

[CryptoAnalyst](https://thecryptoanalyst.medium.com/?source=post_page-----c854f1d2686d-----------------------------------) разместил на Medium статью под названием «[Манифест анонимности](https://thecryptoanalyst.medium.com/the-anonymity-manifesto-c854f1d2686d)», объявив анонимность естественным правом человека, за которое следует бороться. Оригинал манифеста можно найти по [этой ссылке](https://thecryptoanalyst.medium.com/the-anonymity-manifesto-c854f1d2686d).

### _Мероприятия_

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов.

Билеты на MoneroKon теперь можно приобрести здесь, на веб-сайте MoneroKon.

Очередная плановая встреча по проведению MoneroKon 2022 состоится в субботу, 9 апреля 2022 года в 17:00 UTC на IRC-канале #monero-events.

![16](/img/post/2022-04-14-the-monero-moon-38/16.png)  
*https://monerokon.com/*

На прошлой неделе, 7 апреля, в Майами состоялась конференция [Monerotopia](https://monerotopia.com/). Список докладчиков был просто невероятным. Более подробная информация содержится в разделе «Прочие новости» этого бюллетеня.

Также на прошлой неделе в Майями [Guns N’ Bitcoin](https://gunsnbitcoin.com/) провели мероприятие под названием Freedom Tech Trade Show and Conference. В этом году была добавлена тема Monero и были представлены презентации по этой теме, подготовленные такими участниками, как Сет Симмонс (Seth Simmons).

![17](/img/post/2022-04-14-the-monero-moon-38/17.png)  

### _Биржи и предприниматели_

[OrangeFren.com](https://orangefren.com/), сервис, позволяющий проверять актуальный курс быстрого обмена XMR на другие криптовалюты, недавно был обновлен и ожидает соответствующих отзывов от своих пользователей. Теперь сервис предлагает воспользоваться Telegram-ботом, который будет отслеживать изменение цены, а также поддерживает больше различных монет и вариантов обмена. Более подробную информацию вы найдёте [здесь](https://www.reddit.com/r/Monero/comments/tz451y/update_on_orangefrencom_and_request_for_more/).

![18](/img/post/2022-04-14-the-monero-moon-38/18.png)  
*https://orangefren.com/exchange/BTC/XMR/0.1/results*

Как сообщает [zetnip](https://www.reddit.com/r/Monero/comments/u34kc8/no_monero_in_fixedfloat/), биржа Fixed Float в настоящее время не предоставляет услуги по покупке XMR. Вы можете только продать эту криптовалюту. Это странно и заставляет задуматься, действительно ли у бирж имеется столько XMR, сколько ими утверждается.

![19](/img/post/2022-04-14-the-monero-moon-38/19.png)  
*https://www.reddit.com/r/Monero/comments/u34kc8/no_monero_in_fixedfloat/*

monerobull запустил в работу сайт [MoneroSupplies.com](https://monerosupplies.com/), который заинтересует вас, если вы ищете на рынке стикеры Monero. Чтобы посетить их магазин, перейдите по [этой ссылке](https://monerosupplies.com/).

Coincards недавно сообщили, что XMR стала самой популярной монетой, используемой при использовании их сервиса в США.

![20](/img/post/2022-04-14-the-monero-moon-38/20.png)  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![21](/img/post/2022-04-14-the-monero-moon-38/21.png)  

The Monero Moon разместили в CCS очередной запрос на [финансирование следующих 18-ти выпусков](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/294). Если вам нравится читать The Monero Moon, пожалуйста, поддержите наше предложение, оставив свой комментарий. Наш предыдущий запрос в CCS был опубликован [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/blob/master/john-foss-the-monero-moon.md). Дополнительную информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/tkoned/feedback_requested_would_you_like_the_monero_moon/).

moneroist разместил предложение по разработке Patronero, опенсорс-проекта для осуществления пожертвований с помощью майнинга. Подробнее о предложении читайте здесь.

CryptoGrampy опубликовал в системе CCS предложение по созданию браузерного, эфемерного, бессерверного веб-приложения Point of Sale для Monero. С предложением можно ознакомиться [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/307).

Дональд А. Ильязи (Donald A. Iljazi) внёс предложение по переводу приложений, веб-сайтов и прочих материалов на греческий язык. Соответствующее предложение размещено [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/296).

willk опубликовал в CCS предложение под названием «Пусть больше людей пользуются Monero, push-уведомления в Telegram, проведение небольших транзакций за секунды, приватное развёртывание Docker, обеспечение бесплатного сервиса API».

Midipoet собирает средства для посещения [2022 Oslo Freedom Forum](https://hrf.org/category/oslo-freedom-forum/), который пройдёт в период с 23 по 25 мая в Осло. Но конкретно его интересует раздел форума под названием [Financial Freedom Track](https://hrf.org/hrf-and-seetee-present-the-financial-freedom-track-at-off-2022/) (Путь финансовой свободы), где он смог бы донести информацию о такой ориентированной на обеспечение приватности криптовалюте, как Monero.

Предложение m0n3r0d1c3 по оказанию помощи в запуске казино Monero Dice профинансировано.

Предложение [mj](https://repo.getmonero.org/mj) о создании нового проекта под названием [SolOptXMR](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/299) (Оптимальный солнечный майнинг XMR) было перенесено в раздел «Требуется финансирование».

### _Торговля и биржевые спекуляции_

Если криптовалютные биржи занимаются виртуальным трейдингом или голыми шортами XMR, то для выполнения своих обязательств они могут быть вынуждены купить Monero, что ещё больше усилит давление на цену, аналогично тому, как это [случилось с Gamestop в начале 2021 года](https://en.wikipedia.org/wiki/GameStop_short_squeeze), когда около 140% публично размещённых активов GameStop были проданы шортами.

Месячный график XMR/USD демонстрирует бычий тренд. На графике ниже жёлтыми линиями обозначен нисходящий тренд XMR, а кругами - места, где XMR удалось прорваться. И это случилось третий раз за три года. Предыдущие разы XMR выходила из месячного нисходящего тренда, поднимаясь на 110% и 540% с точки такого прорыва.

![22](/img/post/2022-04-14-the-monero-moon-38/22.png)  
*Месячный график XMR/USD с выходами из нисходящего тренда*

Месячный график XMR/BTC со скользящими средними (MA) продемонстрировал обнадёживающие признаки движения вверх. Последний раз 10-месячные MA пересекали 20-месячные MA в 2016 году, и тогда цена XMR резко выросла. Всё выглядит так, как если бы очередное пересечение должно было произойти в ближайшие два месяца.

![23](/img/post/2022-04-14-the-monero-moon-38/23.png)  
*Месячный график XMR/BTC со скользящими средними*

На недельном графике Monero вырвалась из нисходящего тренда по отношению к Ethereum. Наблюдается чёткий ретест и возврат в течение последних двух недель.

![24](/img/post/2022-04-14-the-monero-moon-38/24.png)  
*На недельном графике Monero вырвалась из нисходящего тренда по отношению к Ethereum*

Monero Matteo опубликовал на YouTube видео, в котором прогнозируется бычий тренд Monero. Видео можно найти [здесь](https://www.youtube.com/watch?v=ZCwcYIoviks).

{{< youtube id="ZCwcYIoviks" autoplay="false" >}}  

_**Показатели**_
- Общее количество Monero в обращении: 18 107 158 XMR
- Общая рыночная капитализация Monero: 4 276 342 651 USD
- Позиция в рейтенге Coinmarketcap: 34
- Цена XMR/USD: 235 USD
- Цена XMR/BTC: 0,00572 BTC
- Цена на LocalMonero.co: 244 USD
- Средний размер комиссии за проведение транзакции: 0.00014 XMR ($0.03)
- Хешрейт: 3.067 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![25](/img/post/2022-04-14-the-monero-moon-38/25.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

{{< youtube id="lyDZ-_27Mn4" autoplay="false" >}}  

![26](/img/post/2022-04-14-the-monero-moon-38/26.jpeg)  

![27](/img/post/2022-04-14-the-monero-moon-38/27.jpeg)  

![28](/img/post/2022-04-14-the-monero-moon-38/28.jpeg)  

![29](/img/post/2022-04-14-the-monero-moon-38/29.png)  

![30](/img/post/2022-04-14-the-monero-moon-38/30.jpeg)  

![31](/img/post/2022-04-14-the-monero-moon-38/31.jpeg)  

![32](/img/post/2022-04-14-the-monero-moon-38/32.png)  

![33](/img/post/2022-04-14-the-monero-moon-38/33.jpeg)  

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 38)](https://www.themoneromoon.com/p/the-monero-moon-issue-38)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
