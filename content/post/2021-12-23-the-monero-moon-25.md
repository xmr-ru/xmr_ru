---
title: "The Monero Moon (выпуск 25)"
date: "2021-12-23"
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

_Мы вернулись после пятимесячного перерыва :-)_

### _Разработка, новые версии и технологии_

Встречайте новую версию v0.17.3.0 Oxygen Orion GUI! Более подробную информацию можно найти на [официальном сайте Monero](https://www.getmonero.org/2021/12/04/monero-GUI-0.17.3.0-released.html).

В реализации технологии атомных свопов Monero, финансируемой сообществом Monero, Farcaster, теперь имеется стресс-тест для тестовой сети, то есть, по сути, первая общедоступная версия Farcaster! Попробуйте сами! Более подробную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/rhe6rg/farcaster_node_a_decentralized_p2p_atomic_swap/?utm_source=share&utm_medium=ios_app&utm_name=iossmf) и [здесь](https://github.com/farcaster-project/farcaster-node).

Технология атомных свопов Monero-Ethereum в настоящее время находится на этапе разработки, и разработчики уже достигли больших успехов, поскольку всё уже происходит на низкозатратном уровне 2 Arbitrum Ethereum. Дополнительную информацию можно найти в твите, который приводится ниже.

Член команды лидеров Monero (Monero Core Team) BinaryFate опубликовал [заявление](https://www.getmonero.org/2021/12/06/vulnerability-multisig.html), в котором сообщается, что в реализованной версии кошельков Monero, использующих схему мультиподписи, были обнаружены некоторые уязвимости. Эти уязвимости не влияют на теорию поддержки мультиподписей, но сказываются на текущем коде кошелька, реализующем её. Насколько мне известно, над соответствующим исправлением уже ведётся работа.

Команда Cake Wallet [попросила представителей Inference провести аудит](https://www.reddit.com/r/Monero/comments/rlo8cz/cake_wallet_asked_inference_to_audit_thorchains/) реализации схемы мультиподписи Thorchain для Monero, и результаты оказались вполне хорошими. Thorchain — это децентрализованный протокол обеспечения ликвидности, который довольно точно имитирует пользовательский опыт централизованного обменника. Пользователи могут ввести команду (например: обменять XMR на BTC по этому адресу), затем отправить XMR, и узлы позаботятся об остальной части сделки. Что особенно интересно, так это то, что пользователи смогут обеспечивать ликвидность XMR, не используя «завёрнутый» актив. Безусловно, Monero [необходимо исправить](https://www.getmonero.org/2021/12/06/vulnerability-multisig.html) собственный вариант реализации мультиподписи, прежде чем Thorchain сможет использовать схему мультиподписи Monero. Но конкретные изменения кода Thorchain, уже проанализированы.

Целью Seraphis, «абстракции протокола транзакций», над которой работал Koe, является улучшение ключей Monero. Seraphis определяет правила, согласно которым вы можете разработать реальный (ориентированный на обеспечение приватности) протокол [транзакций](https://www.getmonero.org/resources/moneropedia/transaction.html), не указывая при этом конкретных алгоритмов. Эта разработка [позволяет](https://twitter.com/JEhrenhofer/status/1473714660096589838?s=20) обеспечить унифицированный формат адреса, более правдоподобное отрицание и возможность делиться полной историей кошелька (то есть, полный ключ просмотра).

https://twitter.com/JEhrenhofer/status/1473714660096589838?s=20

Если вы, подобно мне, на последние несколько месяцев выпали из жизни, возможно, вам не известно, что [SChernykh](https://github.com/SChernykh) разработал [децентрализованный майнинг-пул](https://github.com/SChernykh/p2pool) для Monero под названием [P2Pool](https://github.com/SChernykh/p2pool). P2Pool сочетает в себе преимущества пула и соло-майнинга. Вы по-прежнему полностью контролируете свой узел Monero и то, что он добывает, но при этом вы получаете частые выплаты, как в случае с обычным пулом. Никто не сможет использовать ваши майнеры для проведения атаки 51%. Если вы хотите присоединиться к тестированию программного обеспечения, посетите страницу [эту страницу](https://github.com/SChernykh/p2pool) на GitHub, а [здесь](https://www.reddit.com/r/Monero/comments/p9apyd/psa_monero_decentralized_mining_pool_p2pool/) можно найти доходчивую информацию о P2Pool.

[e-mess](https://www.reddit.com/user/e-mess/) с радостью объявили о том, что они выпустили версию 0.99 moner0-python, которая представляет собой комплексную библиотеку Python для работы с Monero. Скачайте её и попробуйте с ней поработать. Более подробную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/rl0ltn/moneropython_099_is_released_testers_welcome/).

В мобильном кошельке [Monerujo](https://monerujo.app/) недавно была реализована поддержка «луковых» узлов — впервые в случае с мобильными кошельками XMR! Эта возможность доступна в [последней стабильной версии](https://github.com/m2049r/xmrwallet/releases/tag/v2.2.1), поэтому скачивайте её и включайте режим шифропанка! Команда Monerujo предлагает вам использовать отличный бесплатный мобильный кошелек, который также поддерживает аппаратные кошельки, так что дерзайте!

Cake Wallet, кошелёк для мобильных пользователей, продолжает развиваться, и команда Cake Wallet уже планирует создать новое приложение, [предназначенное исключительно для Monero](https://www.reddit.com/r/Monero/comments/r6imt9/statement_from_cake_wallet/). Это позволит Cake Wallet не только интегрировать дополнительные криптовалюты в кошелёк, но и удовлетворить насущные потребности энтузиастов из сообщества Monero.

Команда децентрализованной биржи Haveno опубликовала несколько изображений их графического пользовательского интерфейса. Изображение можно найти на их [веб-сайте](https://haveno.exchange/). Кроме того, Haveno всё ещё ищет ведущего разработчика внешнего интерфейса (ReactJS, typescript) или небольшую команду разработчиков для создания пользовательского интерфейса Haveno, и если вы желаете помочь им в этом, то можете оставить свою заявку [здесь](https://www.reddit.com/r/Monero/comments/rj4ax8/haveno_is_still_looking_for_a_frontend_lead/).

![01](/img/post/2021-12-23-the-monero-moon-25/01.png)
_Haveno DEX GUI — https://preview.redd.it/2pq8hmfsg7181.png?width=981&format=png&auto=webp&s=572f545bf61fe5392c8885143900ad4d77f883be_

Количество транзакций Monero в ноябре было рекордно высоким. По умолчанию было проведено просто колоссальное количество приватных транзакций Monero, составившее 916 084 транзакции!

https://twitter.com/DontTraceMeBruh/status/1466048026783408129

RogueMaven представил проект Monero Ilaro. Monero Ilaro — это самозагружаемая ОС Linux и набор инструментов, предназначенных для быстрого освоения Monero новыми пользователями. Всё запускается с USB-накопителя. Более подробную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/rdtnii/project_monero_ilaro_a_bootable_linux_os_and/).

### _Прочие новости_

Проект Monero «с избытком» фигурирует в старом видео на YouTube от [Наоми SexyCyborg Ву](https://www.youtube.com/channel/UCh_ugKacslKhsGGdXP0cRRA), которое снова набирает популярность. У Наоми на YouTube 1,5 миллиона подписчиков. Видео можно посмотреть [здесь](https://www.youtube.com/watch?v=JOfpG37WCLk).

![02](/img/post/2021-12-23-the-monero-moon-25/02.png)
_https://www.youtube.com/watch?v=JOfpG37WCLk_

Контрибьютор Monero Джастин Эренхофер, в [своём сообщении](https://twitter.com/JEhrenhofer/status/1464240109461643275?s=20) в Twitter отмечает, что Финансовая корпорация Америки (FCA) не выдавала Kraken или какой-либо другой фирме никаких конкретных инструкций в отношении Monero.

[Согласно заявлениям FCA](https://twitter.com/JEhrenhofer/status/1464240109461643275?s=20), корпорация не выдавала Kraken или какой-либо другой фирме никаких конкретных инструкций в отношении Monero

Monero Talk недавно взяли интервью у Шри Аравинды Кришнана, постдока в области прикладной криптографии Университета Карнеги-Меллона, также являющегося соавтором различных документов, послуживших основой для разработки второго уровня Monero, известного как платёжные каналы и подобного lighning-сети Bitcoin. Видео можно посмотреть ниже.

Monero Talk

https://youtu.be/8r9i2mTecSA

Сет Симмонс [опубликовал пост](https://blog.sethforprivacy.com/posts/dispelling-monero-fud/#conclusion) под названием «Развеиваем опасения, неуверенность и сомнения, связанные с Monero» (Dispelling Monero FUD), в котором рассматриваются распространённые FUD и даются ответы для каждого из них, а также приводятся ссылки на соответствующие ресурсы. Это отличная статья, которую стоит прочитать и поделиться со всеми теми, кто скептически воспринимает Monero.

О Monero говорится в недавней статье Techcrunch под названием «Massive возьмёт в аренду ваши незанятые вычислительные мощности для оплаты приложений» (Massive wants to rent your spare compute power to pay for apps). «Massive занимается майнингом криптовалют, устойчивых к использованию ASIC, таких как Monero, выбирая их в зависимости от того, что наиболее выгодно на данный момент», и использует их для оплаты приложений вместо с трудом заработанных денег. Ознакомиться со статьёй можно [здесь](https://techcrunch.com/2021/11/30/massive-wants-to-rent-your-spare-compute-power-to-pay-for-apps/).

Monero фигурирует в [недавней статье Slate](https://slate.com/technology/2021/11/monero-privacy-coin-racists-cybercriminals.html) под названием «Конкурент Bitcoin, полюбившийся альтернативным правым и преступникам» (The Bitcoin Competitor Beloved by the Alt-Right and Criminals). В статье Monero осуждается, и автор пытается связать её с преступными и экстремистскими группировками, но при этом никак не освещает положительные аспекты Monero или тот факт, что, если кто-то желает обеспечить собственную приватность, это вовсе не означает, что этот кто-то - преступник.

![03](/img/post/2021-12-23-the-monero-moon-25/03.png)
_https://slate.com/technology/2021/11/monero-privacy-coin-racists-cybercriminals.html_

Хотите подарить Monero кому-то на Рождество? Воспользуйтесь этим [печатным шаблоном](https://www.reddit.com/r/Monero/comments/riurmj/monero_gift_printable/) от phloating_man.

![04](/img/post/2021-12-23-the-monero-moon-25/04.png)
https://www.reddit.com/r/Monero/comments/riurmj/monero_gift_printable/

### _Биржи и предприниматели_

Межсетевой протокол DeFi, Sienna Network, позволил использовать торговые пары Monero на своей децентрализованной бирже, что даёт пользователям возможность совершать приватные сделки, используя две из самых узнаваемых криптовалют в мире. Дополнительную информацию можно получить, ознакомившись с [этой статьёй](https://cointelegraph.com/news/siennaswap-adds-bitcoin-monero-trading-pairs-in-push-for-privacy-focused-defi).

Cake Wallet выпустили видео, демонстрирующее, как обменивать BTC на XMR посредством их мобильного приложения. Видео можно посмотреть по [этой ссылке](https://www.reddit.com/r/Monero/comments/rg7hgh/how_to_new_video_on_how_to_convert_bitcoin_to/). Кроме того, поздравляем команду Cake Wallet с преодолением планки в 200 000 установок на мобильных устройствах!

Cake Wallet был установлен более 200 000 раз на устройства, работающие под iOS и Android!

Теперь вы можете приватно и анонимно обновить свой защищённый почтовый ящик Tutanota, заплатив за сервис при помощи Monero! Более подробную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/rkubnb/tutanota_to_accept_monero_and_bitcoin_as_forms_of/).

VPN сеть Mullvad планирует реализовать поддержку Monero в 2022 году.

![04](/img/post/2021-12-23-the-monero-moon-25/04.png)
https://www.reddit.com/r/Monero/comments/rm36jo/mullvad_vpn_to_add_monero_in_2022/

### _Краудфандинговая система сообщества (CCS)_

На странице системы CCS Monero размещён целый ряд предложений, открытых для обсуждения. Среди них реализация атомных свопов XMR-ETH и проведение конференции MoneroKon 2022. Со всеми предложениями можно ознакомиться [здесь](https://ccs.getmonero.org/ideas/).

### _Торговля и биржевые спекуляции_

[BackDownBear](https://www.tradingview.com/u/BackDownBear/) представил биржевые спекуляции в форме фрактального графика относительно возможного пути XMR к цене $4000 USD. Соответствующий пост размещён [здесь](https://www.tradingview.com/chart/XMRUSDT/7AV2fUOF-XMR-To-4K-The-Age-Of-Privacy/).

![05](/img/post/2021-12-23-the-monero-moon-25/05.png)
_https://www.tradingview.com/chart/XMRUSDT/7AV2fUOF-XMR-To-4K-The-Age-Of-Privacy/_

_**Показатели**_
Общее количество Monero в обращении — 18 051 278 XMR
Общая рыночная капитализация Monero — $3 778 307 145 USD
Цена XMR/USD — $208 USD
Цена XMR/BTC — 0,00409 BTC
Цена на LocalMonero.co — $237 USD
Средний размер комиссии за проведение транзакции — 0,00013 XMR ($0,027)
Хешрейт — 2,952 Ghash/s
Распределение хешрейта между пулами для майнинга Monero

![06](/img/post/2021-12-23-the-monero-moon-25/06.png)

### _Для развлечения_

![07](/img/post/2021-12-23-the-monero-moon-25/07.jpg)

![08](/img/post/2021-12-23-the-monero-moon-25/08.jpg)

![09](/img/post/2021-12-23-the-monero-moon-25/09.jpg)
_Надпись на транспаранте: «Частные и неотслеживаемые криптовалюты опасны для криминальных государств и препятствуют порабощению людей центральными банками» — https://www.reddit.com/r/Monero/comments/qzyhcn/monero_sign_private_and_untraceable/_

![10](/img/post/2021-12-23-the-monero-moon-25/10.jpg)

![11](/img/post/2021-12-23-the-monero-moon-25/11.jpg)

![12](/img/post/2021-12-23-the-monero-moon-25/12.jpg)

---

Приносим извинения за задержку выпуска, если вы ждали его! Иногда всё идёт не так, как задумано, но я всеми силами постараюсь регулярно публиковать The Monero Moon в течение 2022 года!

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`
---

_Источник: [What is Seraphis, and Why Should You Care?](https://www.getmonero.org/2021/12/22/what-is-seraphis.html)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
