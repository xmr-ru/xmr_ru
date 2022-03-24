---
title: "The Monero Moon (выпуск 34)"
date: "2022-03-17"
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

selsta поделился новостями о своей работе в качестве разработчика. В процессе подготовки к очередному обновлению сети Monero selsta занимался отладкой GUI-кошелька и завершил переработку мнемонической фразы. Более подробную информацию можно найти [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/279#note_15401) или по ссылке, которая приводится ниже.

![01](/img/post/2022-03-17-the-monero-moon-34/01.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/279#note_15401*

Джастин Берман разместил отчёт по своей работе над развитием Monero. Отдельно стоит отметить пул-реквест для увеличения размера кольца Monero до 16! Более подробно об этом можно прочитать [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/285#note_15356).

![02](/img/post/2022-03-17-the-monero-moon-34/02.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/285#note_15356*

Вышла версия v2.4.1 Baldaŭ Monerujo! Monerujo — это Android-кошелёк Monero, помимо прочего поддерживающий аппаратный кошелёк Ledger. Среди доступных обновлений множество цветовых тем и некоторые исправления UI. Дополнительную информацию о новой версии можно найти [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/295).

![03](/img/post/2022-03-17-the-monero-moon-34/03.png)  
*https://www.monerujo.io/*

Haveno, некастодиальная децентрализованная биржа, построенная на основе Monero и Tor, недавно поделилась своими планами по разработке пользовательского интерфейса и функций, работающих с клиентской стороны. Вы можете прочитать больше об их работе и ознакомиться с соответствующим предложением CCS по этой [ссылке](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/295).

[Одному майнеру Monero посчастливилось](https://www.reddit.com/r/Monero/comments/te2vuj/i_solo_mined_a_block_in_less_than_a_week_using_a/) добыть блок в режиме соло-майнинга менее чем за неделю с помощью одного единственного PC с процессором Ryzen 5 3600 при хешрейте примерно 2500 H/s!

![04](/img/post/2022-03-17-the-monero-moon-34/04.jpeg)  
*https://www.reddit.com/r/Monero/comments/te2vuj/i_solo_mined_a_block_in_less_than_a_week_using_a/*

В целях обеспечения безопасности сети Monero настоятельно рекомендуется создать собственный узел. Вы также можете заняться соло-майнингом с помощью официального GUI-кошелька Monero, который можно скачать [здесь](https://www.getmonero.org/downloads/), или же вы можете делать это в пуле, присоединившись к децентрализованному и не требующему каких-либо специальных разрешений пулу [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html). Вы даже можете заниматься майнингом XMR на своём [мобильном устройстве](https://www.reddit.com/r/MoneroMining/comments/srjwg0/direct_upload_how_to_mine_monero_on_an_old/)! Официальный веб-сайт Monero [getmonero.org](https://www.getmonero.org/get-started/mining/) — самое подходящее из возможных мест, чтобы начать заниматься майнингом, воспользовавшись размещённой на нём информацией.

CryptoGrampy занимается разработкой узла GUI Monero для Android (в соответствии с опубликованным в CCS запросом о финансировании). На этой неделе [CryptoGrampy](https://twitter.com/CryptoGrampy/status/1502093717313835011?s=20&t=DB__qL6j-ALNO0a9BOHZIQ) сообщил всем через Twitter, что уже приступил к работе над обновлением UX и функций старого Android-узла Aeon, архив с которым он нашёл на GitHub, и что надеется [адаптировать его для Monero](http://ttps//twitter.com/CryptoGrampy/status/1502093905558388737/photo/1).

![05](/img/post/2022-03-17-the-monero-moon-34/05.png)  
*https://twitter.com/CryptoGrampy/status/1502093905558388737/photo/1*

hinto-janaiyo опубликовал XMRig-Auto-Build v1.2. XMRig-Auto-Build — это bash-скрипт, позволяющий построить самый последний XMRig непосредственно на основе исходного кода. Вы найдёте его [здесь](https://github.com/hinto-janaiyo/XMRig-Auto-Build)!

![06](/img/post/2022-03-17-the-monero-moon-34/06.png)  
*https://github.com/hinto-janaiyo/XMRig-Auto-Build*

Появилась версия v2.0 xmrsale, лёгкого платёжного процессора с плагином woocommerce, позволяющим абсолютно любому принимать Monero. Несмотря на то, что xmrsale призывают пользователей создавать собственные узлы, они понимают, что далеко не каждый может себе это позволить. Поэтому после обновления вы сможете пользоваться xmrsale, не создавая собственного узла Monero.
Найти xmrsale можно по этой [ссылке](https://xmrsale.org/).

![07](/img/post/2022-03-17-the-monero-moon-34/07.png)  
*https://xmrsale.org/*

Monero Observer опубликовали [отчёт по разработке Monero за 10-ю неделю 2022 года](https://www.monero.observer/monero-dev-activity-report-week-10-2022/). Это прекрасный обзор деятельности разработчиков Monero. Более подробно об этом можно узнать по этой [ссылке](https://www.monero.observer/monero-dev-activity-report-week-10-2022/).

![08](/img/post/2022-03-17-the-monero-moon-34/08.png)  
*https://www.monero.observer/monero-dev-activity-report-week-10-2022/*

### _Прочие новости_

Теперь Monero официально принимают в качестве пожертвования на государственном уровне.

![09](/img/post/2022-03-17-the-monero-moon-34/09.png)  
*https://donate.thedigital.gov.ua*

Вещание XMR.radio теперь осуществляется по I2P и через Tor. Послушать их можно [здесь](http://xmr.radio/), а ссылки на потоковое вещание I2P и Tor размещены [здесь](https://www.reddit.com/r/Monero/comments/te4wqz/xmrradio_now_streaming_over_i2p/).

О Monero было много сказано в статье «Что сталось с мечтой о приватной криптовалюте?» ([What Happened to the Dream of Private Cryptocurrency](https://www.vice.com/en/article/v7dqk8/what-happened-to-the-dream-of-private-cryptocurrency)), опубликованной Motherboard. Это великолепная статья, в которой обсуждается, какое место Monero и технологии обеспечения приватности занимают в современном мире и как они развиваются. Также в статье приводятся цитаты Сета Симмонса и Вика Шармы, являющихся приверженцами идей Monero и часто упоминающих об уникальности этой криптовалюты.

![10](/img/post/2022-03-17-the-monero-moon-34/10.png)  
*Комментарий Сета Симмонса, который приводится в статье «[Что сталось с мечтой о приватной криптовалюте?](https://www.vice.com/en/article/v7dqk8/what-happened-to-the-dream-of-private-cryptocurrency)», опубликованной Motherboard.*

Bitcoin.com опубликовали статью под названием «Несмотря на кризис глобальной экономики, приватные криптоактивы XMR, ZEC демонстрируют двузначный рост» ([Privacy Crypto Assets XMR, ZEC See Double-Digit Gains Amid Tightened Global Economy](https://news.bitcoin.com/privacy-crypto-assets-xmr-zec-see-double-digit-gains-amid-tightened-global-economy/)). Статью можно найти [здесь](https://news.bitcoin.com/privacy-crypto-assets-xmr-zec-see-double-digit-gains-amid-tightened-global-economy/).

![11](/img/post/2022-03-17-the-monero-moon-34/11.png)  

Команда [Wasabi Wallet](https://twitter.com/wasabiwallet/status/1503091503207432193?s=20&t=SmPNLlqm_cpcin7A_7zgdw), ориентированного на обеспечение приватности Bitcoin-кошелька, использующего не требующую доверия технологию CoinJoin, объявила о том, что собирается отказаться от регистрации непотраченных выходов транзакций (UTXO) в coinjoins. Разработчик Wasabi nopara73 заявил, что это «основное препятствие с точки зрения взаимозаменяемости Bitcoin». Пользователи кошелька Wasabi уже столкнулись с [заморозкой своих счетов](https://sethforprivacy.com/posts/fungibility-graveyard/#wasabi) такими биржами, как Binance и Bitfinex, за вывод BTC на Wasabi или даже попытку перевести BTC на кошелёк Wasabi. К сожалению для команды Wasabi, им придётся непросто, когда они попытаются привлечь новых или вернуть старых пользователей.

![12](/img/post/2022-03-17-the-monero-moon-34/12.png)  

![13](/img/post/2022-03-17-the-monero-moon-34/13.png)  
*https://t.me/WasabiWallet/63992*

Издание The Financial Times опубликовало статью под названием «NCA призывает к регулированию криптовалютных миксеров, используемых для «вспенивания» криминальной валюты» (NCA calls for regulation of crypto mixers used in ‘churning criminal cash’). В статье подробно рассказано о том, почему Национальное агентство по борьбе с преступностью Великобритании (NCA) призывает к регулированию сложной технологии смешивания, которая используется преступниками при отмывании денег с помощью криптовалют.

Комитет Европейского парламента по экономическим и валютным вопросам проголосовал против запрета использования активов, в основе которых лежит алгоритм доказательства работы, компаниями, расположенными в Европейском Союзе.

![14](/img/post/2022-03-17-the-monero-moon-34/14.png)  

Агентство Reuters сообщает, что украинские пограничники изъяли «16 килограмм золота, десятки тысяч долларов и евро, а также тысячи упаковок сигарет у украинских дипломатов, которые пытались контрабандой ввести их в Польшу». Интересно, если бы у них были приватные ключи Monero или другой криптовалюты при пересечении границы, пришлось бы им столкнуться с подобной проблемой?

![15](/img/post/2022-03-17-the-monero-moon-34/15.png)  
*https://www.reuters.com/article/us-ukraine-smuggle-diplomats-idUSKCN2AT2L1*

Н. С. Лайонс опубликовал статью «Просто скажите «нет» CBDC» ([Just Say No to CBDCs](https://theupheaval.substack.com/p/just-say-no-to-cbdcs?s=r)). Это развлекательная антиутопия, за которой следует содержательное обсуждение того негативного влияния, которое может оказать выпуск цифровой валюты центральным банком (CBDC) на общество.

![16](/img/post/2022-03-17-the-monero-moon-34/16.png)  

Оказавшийся комиком политический активист Рассел Бренд опубликовал на YouTube видео, в котором оспаривает необходимость во внедрении и использовании криптовалют в качестве инструмента, который можно использовать для обеспечения свободы и защиты от давления со стороны правительства.

{{< youtube id="V4VXWdWMLvA" autoplay="false" >}}
*https://www.youtube.com/watch?v=V4VXWdWMLvA*

MAGIC Grants, общественная благотворительная организация, занимающаяся выплатой грантов студентам, интересующимся криптовалютами, и поддержкой различной критически важной публичной криптовалютной платёжной инфраструктуры, сообщает о накоплении более 74 XMR на своём балансе.

![17](/img/post/2022-03-17-the-monero-moon-34/17.png)  

### _Мероприятия_

Очередная плановая встреча по проведению MoneroKon 2022 состоится в воскресенье, 20 марта 2022 года в 18:00 UTC на IRC-канале #monero-events. Помимо этого, вы узнаете больше о конференции Monero, которая пройдёт в Лиссабоне в июне 2022, если посетите веб-сайт MoneroKon 2022. Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров.

![18](/img/post/2022-03-17-the-monero-moon-34/18.png)  
*https://monerokon.com/*

7 апреля в Майями состоится мероприятие под названием [Monerotopia](https://monerotopia.com/), где выступит множество интересных докладчиков, среди которых будет даже [Crytp0 Bear](https://www.youtube.com/channel/UCWC1InTHly5Tg-7e5P_S5Rw). Посетите их [веб-сайт](https://monerotopia.com/) и приобретите билет на одну из самых жарких конференций Monero!

![19](/img/post/2022-03-17-the-monero-moon-34/19.png)  
*https://monerotopia.com/*

9-10 апреля в Майями [Guns N’ Bitcoin](https://gunsnbitcoin.com/) проведут мероприятие под названием Freedom Tech Trade Show and Conference. В этом году будет добавлена тема Monero, а на конференции выступят представители сообщества Monero. Более подробную информацию можно найти [здесь](https://gunsnbitcoin.com/).

![20](/img/post/2022-03-17-the-monero-moon-34/20.png)  
*https://gunsnbitcoin.com/*

### _Биржи и предприниматели_

MoneroUK разместил на YouTube видеоруководство, в котором разъясняется, как обменять BTC на XMR посредством Cake Wallet.

{{< youtube id="hvhy0gCmwGs" autoplay="false" >}}  
*https://www.youtube.com/watch?v=hvhy0gCmwGs*

### _Краудфандинговая система сообщества (CCS)_

Открыто финансирование по запросу [koe](https://repo.getmonero.org/koe), который будет работать над доказательством концепции кошелька Seraphis. Средства можно пожертвовать [здесь](https://ccs.getmonero.org/proposals/seraphis-wallet-poc.html).

Предложение по финансированию The Monero Observer на весну 2022 года одобрено, и сбор пожертвований начат. Финансово поддержать их работу можно по этой [ссылке](https://ccs.getmonero.org/proposals/escapethe3ra-monero-observer-maintenance-spring-2022.html).

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![21](/img/post/2022-03-17-the-monero-moon-34/21.png)  
*https://ccs.getmonero.org/*

CryptoGrampy предложил выплатить премию за разработку узла GUI для Android. Подробнее об этом можно узнать [здесь](https://bounties.monero.social/posts/59/android-gui-monero-node).

[Winston](https://repo.getmonero.org/winstonsthiccbooty) также разместил в CCS запрос о финансировании разработки FOSS-приложения для Android под названием Whatnero, в котором будет собрана и в удобной форме представлена вся доступная информация о Monero, чтобы новичкам или экспертам было проще найти нужную им информацию. С предложением можно ознакомиться по этой [ссылке](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/293).

Haveno разместили запрос о финансировании разработки их пользовательского интерфейса и функций, работающих с клиентской стороны. Более подробно обо всём можно узнать в их [предложении](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/295), размещённом здесь в CCS.

Наконец The Monero Moon также разместили в CCS [очередной запрос на финансирование следующих 18-ти выпусков](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/294). Если вам нравится читать The Monero Moon, пожалуйста, поддержите наше предложение, оставив свой комментарий. Наш предыдущий запрос в CCS был опубликован здесь.

### _Торговля и биржевые спекуляции_

Ежедневный график пары XMR/USD образовал восходящий треугольник. Это окончательно обозначившийся бычий тренд. Целевая планка — 300+ USD.

![22](/img/post/2022-03-17-the-monero-moon-34/22.png)  

[DonYakka](https://www.tradingview.com/chart/XMRUSD/dLucc3bk-XMR-USD/) опубликовал график с прогнозом бычьего изменения цены XMR. Потенциальный рост цены находится в четырёхзначном диапазоне.

![23](/img/post/2022-03-17-the-monero-moon-34/23.png)  
*https://www.tradingview.com/chart/XMRUSD/dLucc3bk-XMR-USD/*

![24](/img/post/2022-03-17-the-monero-moon-34/24.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 093 829 XMR
- Общая рыночная капитализация Monero: 3 387 942 048 USD
- Цена XMR/USD: 188 USD
- Цена XMR/BTC: 0,004505 BTC
- Цена на LocalMonero.co: 203 USD
- Средний размер комиссии за проведение транзакции: 0.00013 XMR ($0.025)
- Хешрейт: 2.968 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![25](/img/post/2022-03-17-the-monero-moon-34/25.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![26](/img/post/2022-03-17-the-monero-moon-34/26.jpeg)  
*https://www.reddit.com/r/Monero/comments/tdhso5/spotted_in_stockholm_this_evening/*

![27](/img/post/2022-03-17-the-monero-moon-34/27.jpeg)  
*https://twitter.com/MoneroArchive/status/1503121123332001799/photo/1*

![28](/img/post/2022-03-17-the-monero-moon-34/28.png)  
*https://www.reddit.com/r/moonero/comments/n69lca/dont_even_bother/*

![29](/img/post/2022-03-17-the-monero-moon-34/29.png)  
*https://twitter.com/DontTraceMeBruh/status/1504242554174427138*

![30](/img/post/2022-03-17-the-monero-moon-34/30.jpeg)   
*https://www.reddit.com/r/moonero/comments/ocygky/nice_privacy_you_got_there_bitcoin_users/*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 34)](https://www.themoneromoon.com/p/the-monero-moon-issue-34)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
