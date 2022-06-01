---
title: "The Monero Moon (выпуск 44)"
date: "2022-05-26"
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

Официальный аккаунт Monero в Twitter недавно провёл сессию вопросов и ответов в Twitter Spaces, в рамках которой обсуждалось очередное обновление сети. Полное обсуждение можно послушать через твит, опубликованный ниже!

![01](/img/post/2022-05-26-the-monero-moon-44/01.png)  

И если вы ещё не в курсе, 16 июля 2022 года на высоте блока 2 668 888 состоится согласованное сообществом Monero обновление сети (хардфорк), призванное повысить уровень приватности и общей производительности. Всем пользователям необходимо обновить программное обеспечение. Новая версия v0.18 Fluorine Fermi будет опубликована за месяц до сетевого обновления, то есть примерно 16 июня. В рамках обновления будет реализован целый ряд новых функций, среди прочего:
- размер кольца будет увеличен с 11 до 16 в целях повышения приватности;
- будут реализованы теги просмотра, в результате чего время синхронизации сократится на 40%;
- после введения Bulletproofs+ размер транзакций уменьшится примерно на 7%, равно как и время верификации, которое также сократится на 7%.

Также вместе с новым программным обеспечением вскоре будет опубликован полный список улучшений и усовершенствований. Если вы хотите узнать больше о грядущем обновлении сети Monero, пожалуйста, ознакомьтесь с [этим постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html) на официальном [веб-сайте Monero](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html). Вы также можете прочитать [журнал встречи](https://github.com/monero-project/meta/issues/684) разработчиков Monero, состоявшейся 16 апреля, на которой обсуждалось данное обновление сети.

![02](/img/post/2022-05-26-the-monero-moon-44/02.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*

Если вы желаете помочь с обновлением сети Monero, достаточно просто уведомить о нём провайдеров кошельков и биржевых сервисов. Пожалуйста, сверьтесь с этим [контрольным листом](https://github.com/monero-project/meta/issues/690), чтобы все надлежащим образом обновили своё программное обеспечение и внесли соответствующие изменения.

![03](/img/post/2022-05-26-the-monero-moon-44/03.png)  
*https://github.com/monero-project/meta/issues/690*

Кроме того, вы можете помочь в тестировании и выявить ошибки в основной версии протокола Monero. Сделать это можно в тестовой сети. Соответствующие тестовые средства (tXMR) доступны абсолютно любому желающему! Дополнительную информацию, связанную с возможным оказанием помощи можно найти в [этом посте, опубликованном garth_xmr](https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/).

![04](/img/post/2022-05-26-the-monero-moon-44/04.png)  
*https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/*

Seth For Privacy также просит протестировать код Monero. Он попытался максимально упростить процесс, опубликовав новый образ Docker, так что абсолютно любой, использующий Ubuntu, может просто перейти по ссылке, указанной выше, и сделать всё, как надо. Если же вы пользуетесь другой операционной системой, например Windows, [свяжитесь с Seth](https://www.reddit.com/r/Monero/comments/utzyyz/help_test_out_the_upcoming_monero_network_upgrade/), и он сделает всё возможное, чтобы помочь вам.

![05](/img/post/2022-05-26-the-monero-moon-44/05.png)  
*https://paste.sethforprivacy.com/?96466ca9ad3f3d90#4fTCXio2b3S6fX5b2YHffzY6zpYsj3bJrgZh7Gmi8ESC*

[noot](https://github.com/noot), также известная как [elizabethereum](https://www.reddit.com/user/elizabethereum/), поделилась новостями о реализации возможности проведения атомных свопов ETH-XMR и заявила, что начальная версия уже развёрнута в Goerli (тестовой сети Ethereum) и отладочной сети Monero. И теперь в отладочной сети требуется помощь по тестированию свопов. Просим по возможности протянуть руку помощи. Тестирование крайне важно, поскольку позволит выявить любые существующие ошибки, чтобы их можно было затем исправить, а также чтобы собрать информацию о пользовательском опыте взаимодействия в целом. Всю дополнительную можно найти [здесь](https://www.reddit.com/r/Monero/comments/ux6lzk/ethxmr_atomic_swap_development_update_live_on/) и [здесь](https://github.com/noot/atomic-swap/blob/master/docs/stagenet.md)!

![06](/img/post/2022-05-26-the-monero-moon-44/06.png)  
*Атомные свопы ETH-XMR: https://github.com/noot/atomic-swap/blob/master/docs/stagenet.md*

Кроме того, elizabethereum недавно выступила на конференции Monerotopia, и её выступление было посвящено именно атомным свопам ETH-XMR.

{{< youtube id="1u0VfkYuXu8" autoplay="false" >}}  

spirobel работает над реализацией браузерного кошелька Monero, подобного Metamask, который сделает регистрацию на веб-сайтах проще и позволит проводить транзакции «в один клик». При этом приватность финансовой информации пользователей никак нарушена не будет. Также ведётся работа над поддержкой NFT. Более подробную информацию можно найти по [этой](https://spirobel.substack.com/p/solving-the-web3-privacy-problem?r=udmo4&s=w&utm_campaign=post&utm_medium=web) и [этой](https://github.com/spirobel/monero-playground) ссылке, а также в соответствующем твите и видео, опубликованном на YouTube и размещённом ниже.

![07](/img/post/2022-05-26-the-monero-moon-44/07.jpg)  

{{< youtube id="4DLcsQ45zoE" autoplay="false" >}}  

[hinto-janaiyo](https://github.com/hinto-janaiyo/monero-gpg) выпустил первую версию [monero-gpg](https://github.com/hinto-janaiyo/monero-gpg), Bash-скрипта, который посредством GPG подписывает сообщения или файлы и содержит текущую статистику по блокам Monero. Со слов hinto-janaiyo, «крутым побочным продуктом доказательства работы является возможность использования хешей блоков в качестве некоего «временного минимума». Если включить хеш блока в сообщение, это будет означать, что такое сообщение было как минимум создано в момент попадания блока в сеть. Чтобы подделать сообщение в будущем, будет необходимо знать хеш каждого блока, который позволит выйти на этот блок, и это включает в себя знание хеша RandomX и всех транзакций».

![08](/img/post/2022-05-26-the-monero-moon-44/08.png)  
*https://github.com/hinto-janaiyo/monero-gpg*

Вы можете так автоматизировать свой узел Monero, чтобы он запускался в фоновом режиме всякий раз, когда вы будете включать свой PC, и перезапускался в случае сбоя. Узнать, как это сделать, можно на Monero Guides.

{{< youtube id="vTNJWubZJks" autoplay="false" >}}  

Знаете ли вы, что можете поддержать сеть Monero путём майнинга через P2Pool с помощью официального GUI-кошелька Monero? Если нет, обязательно ознакомьтесь с [этим постом](https://www.reddit.com/r/Monero/comments/uxcmy7/p2pool_im_in_guys_it_will_run_everyday/), опубликованным Unhappy-Cat2935.

![09](/img/post/2022-05-26-the-monero-moon-44/09.png)  
*https://www.reddit.com/r/Monero/comments/uxcmy7/p2pool_im_in_guys_it_will_run_everyday/*

Inevitable-Fig6717 продемонстрировал сообществу, как занимается майнингом Monero посредством своего мобильного устройства. Если вы хотите таким же образом настроить и своё мобильное устройство, вам понадобится [XMRig для Android](https://github.com/XMRig-for-Android/xmrig-for-android).

![10](/img/post/2022-05-26-the-monero-moon-44/10.png)  
*https://www.reddit.com/r/MoneroMining/comments/ut4cg4/phone_mining_anyone/*

Если вы не можете запустить собственный узел Monero, но хотите выбрать один из узлов, чтобы пользоваться им со своим кошельком, заходите на [monero.fail](https://monero.fail/). Там вы найдёте список узлов, имеющихся в основной, тестовой и отладочных сетях, а также сетевых и луковых узлов.

![11](/img/post/2022-05-26-the-monero-moon-44/11.png)  
*https://monero.fail/*

На monero.fail также можно найти крутую карту, на которой показаны все узлы, имеющиеся в мире! Это более 11 000 узлов. Может, вы найдёте на этой карте и свой родной город!

![12](/img/post/2022-05-26-the-monero-moon-44/12.png)  
*https://monero.fail/map*

spackleXMR прочитал и опубликовал на YouTube главу «Monero с нуля», посвящённую модульной арифметике. Также был показан код Python и использованы некоторые источники, которые помогли проиллюстрировать материал. Видео можно посмотреть [здесь](https://www.reddit.com/r/Monero/comments/uvg2dq/talking_through_zero_to_monero_modular_arithmetic/) или ниже.

{{< youtube id="wDRX27T69tw" autoplay="false" >}}  

Разработка торговой точки Monero, которой занимается Grampy, уверенно продвигается. Все последние новости, связанные с ней, публикуются в Twitter!

![13](/img/post/2022-05-26-the-monero-moon-44/13.png)  

Вышла версия v2.4.3 Monerujo. Были исправлены небольшие недочёты в UI, а также добавлены переводы на фарси и тамильский языки! Новую версию можно скачать [здесь](https://github.com/m2049r/xmrwallet/releases/tag/v2.4.3).

![14](/img/post/2022-05-26-the-monero-moon-44/14.png)  

Вышла версия v1.2.0 Shruum Wallet, форка Monerujo, с дополнительными возможностями обеспечения безопасности, достигаемыми за счёт добавления и удаления некоторых функций. Была удалена возможность аутентификации с помощью отпечатка пальца и поддержка OpenAlias. Дополнительную информацию можно найти в [этом посте](https://www.reddit.com/r/Monero/comments/uveju6/shruum_v120_released_a_hardened_fork_of_monerujo/).

Команда MyMonero собирается выпустить обновлённую версию кошелька для iOS и ищет людей, которые бы помогли с тестированием приложения. Прочитать соответствующий пост и связаться с ними можно по этой ссылке.

Вышли и доступны для скачивания Cake Wallet 4.4.1 и Monero.com 1.0.6. В новых версиях была добавлена поддержка SideShift и исправлены ошибки в Yat.

![15](/img/post/2022-05-26-the-monero-moon-44/15.png)  

Выбираете для себя кошелёк Monero? Тогда, если вас волнуют вопросы сохранения приватности, сообщество рекомендует выбрать кошелёк, при использовании которого вам не придётся делиться никакими приватными ключами просмотра.

Новость, не связанная напрямую с Monero (отчасти потому, что блокчейн-эксплореры Monero в принципе не существуют, потому что Monero очень приватна): hoiru создал поисковый движок, позволяющий найти пользователя Twitter, а также выяснить, публиковал ли когда-нибудь такой пользователь криптовалютный адрес. И если да, вы сможете просмотреть контент, размещённый им в социальной сети, и, просмотрев блокчейн, узнать, сколько средств имеется по такому адресу. Подробности можно найти [здесь](https://iseeyour.cash/)!

![16](/img/post/2022-05-26-the-monero-moon-44/16.png)  
*https://iseeyour.cash/*

[The Monero Observer](https://www.monero.observer/) опубликовали очередной отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://www.monero.observer/monero-dev-activity-report-week-20-2022/).

### _Прочие новости_

На этой неделе Monero Talk опубликовали массу материала, и несмотря на то, что, как правило, мы не уделяем слишком много внимания одному новостному источнику, мы считаем, что должны отдать должное качественному контенту, созданному ими, в частности, связанному с конференцией Monerotopia.

Monero Talk опубликовали видео с конференции Monerotopia, прошедшей в апреле, с выступлением Викранта Шарма (Vikrant Sharma) (основателя и гендиректора Cake Wallet), Майка Олтофа (Mike Olthoff) (основателя и гендиректора CoinCards) и Гаррета Си (Garrett See) (сооснователя Dvchain). Речь шла о построении циркулярной экономики Monero.

{{< youtube id="Smn7BualIzc" autoplay="false" >}}  

Monero Talk также опубликовали видео с Seth for Privacy, в котором говорилось о том же.

{{< youtube id="mvHbGTm9PrE" autoplay="false" >}}  

Помимо прочего, Monero Talk разместили новый эпизод с Monerotopia, в котором обсудили с afungible и Midipoet проблемы цены, а также поговорили о MoneroKon 2022. Видео можно посмотреть [ниже](https://simplehold.io/blog/article/top-5-Community-driven-cryptocurrencies-in-2022?utm_source=social&utm_medium=reddit&utm_campaign=education_post).

{{< youtube id="e0cdExAkG5g" autoplay="false" >}}  

Monero упоминается в статье, опубликованной SimpleHold, под названием «5 лучших криптовалют 2022 года, управляемых сообществом» (Top 5 Community-Driven Cryptocurrencies in 2022). Статью можно найти [здесь](https://simplehold.io/blog/article/top-5-Community-driven-cryptocurrencies-in-2022?utm_source=social&utm_medium=reddit&utm_campaign=education_post).

![17](/img/post/2022-05-26-the-monero-moon-44/17.png)  
*https://simplehold.io/blog/article/top-5-Community-driven-cryptocurrencies-in-2022?utm_source=social&utm_medium=reddit&utm_campaign=education_post*

[The Open Economy Initiative](https://www.youtube.com/c/TheOpenEconomyInitiative) поделились на YouTube видео с некоторыми из последних новостей и событий, связанных с сообществом Monero. Смотрите видео ниже.

{{< youtube id="J2T2cthhdX4" autoplay="false" >}}  

Опубликован [121-й выпуск](https://revuo-xmr.com/issue-121.html) Revuo Monero, еженедельного новостного издания, посвящённого XMR.

ChangeNow опубликовали статью «Приватные монеты в 2022 году: технология, использование и вызовы» (Privacy Coins in 2022: Tech, Use Cases, and Challenges), в которой говорится о Monero. Найти и прочитать статью можно по этой [ссылке](https://changenow.io/blog/privacy-coins-in-2022-tech-use-cases-and-challenges).

Джастин Эренхофер (Justin Ehrenhofer) разоблачил Bitcoin, указав на отсутствие приватности этой криптовалюты. А всё дело в том, что один из пользователей Bitcoin был обвинён в осознанном нарушении санкций Управления по контролю за иностранными активами, передав Bitcoin на сумму более 10 миллионов USD в страну, находящуюся под санкциями.

![18](/img/post/2022-05-26-the-monero-moon-44/18.png)  

### _Мероприятия_

Следующая встреча рабочей группы сообщества Monero запланирована на воскресенье, 29 мая (18:00 UTC) на IRC-канале #monero-events. Присоединяйтесь! Будут обсуждаться обновления в системе CCS, новости сообщества и отчёты рабочих групп. Дополнительную информацию можно найти по [этой ссылке](https://github.com/monero-project/meta/issues/707).

![19](/img/post/2022-05-26-the-monero-moon-44/19.png)  
*https://github.com/monero-project/meta/issues/707*

8 июня в Нью-Йорке, Колорадо, Лас-Вегасе, Чикаго и других местах состоится Глобальное празднование (встреча по поводу) дня начала постэмиссии. Вы также можете отпраздновать окончание номинальной эмиссии Monero и начало постэмиссии со своим местным сообществом XMR! Вы даже можете организовать собственную встречу в своём городе! Всю дополнительную информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/). Свяжитесь с @[chowbungaman](https://www.reddit.com/u/chowbungaman/) через [Telegram-канал Monerotopia](https://t.me/monerotopia) или через Matrix, если хотите организовать собственную встречу или присоединиться к организованной другими. Вы также можете связаться с ними по электронной почте: [monerotopia@protonmail.com](mailto:monerotopia@protonmail.com).

![20](/img/post/2022-05-26-the-monero-moon-44/20.png)  
*https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/*

Очередная плановая встреча по проведению конференции MoneroKon 2022 состоится в субботу, 28 мая 2022 года в 18:00 UTC на IRC-канале #monero-events.

![21](/img/post/2022-05-26-the-monero-moon-44/21.png)  
*https://monerokon.com/*

Конференция Monerokon пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если же вы хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Следует отметить, что билеты на Monerokon 2022 уже распроданы, но могут появиться дополнительные билеты.

![22](/img/post/2022-05-26-the-monero-moon-44/22.png)  

### _Биржи и предприниматели_

Если вы хотите что-то продать или купить за Monero, следите за веткой Friday Monero Market Thread на r/Monero. Ссылку на последнюю пятничную встречу можно найти [здесь](https://www.reddit.com/r/Monero/comments/utnijb/friday_monero_market_thread_may_20_2022/).

![23](/img/post/2022-05-26-the-monero-moon-44/23.png)  
*https://www.reddit.com/r/Monero/comments/utnijb/friday_monero_market_thread_may_20_2022/*

В ShopinBit появилась 21 000 новых косметических товаров и средств личной гигиены. Вы можете купить их за XMR с 3% скидкой!

CBD4Coins теперь продают товары за XMR. Вы можете получить 10% при оплате. Также доступна бесплатная доставка. Всю необходимую информацию можно получить, ознакомившись с [этим постом](https://www.reddit.com/r/Monero/comments/uxl7b8/adoption_buy_cbd_with_xmr/).

Пользователи рынка даркнета всё чаще используют Monero вместо Bitcoin.

![24](/img/post/2022-05-26-the-monero-moon-44/24.png)  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![25](/img/post/2022-05-26-the-monero-moon-44/25.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![26](/img/post/2022-05-26-the-monero-moon-44/26.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![27](/img/post/2022-05-26-the-monero-moon-44/27.png)  
*https://ccs.getmonero.org/funding-required/*

Кроме того, премию в размере 5 XMR получит тот, кто поможет исправить неполадки с веб-сайтом для сбора пожертвований [Monero Bounties](https://bounties.monero.social/). Более подробную информацию можно узнать, ознакомившись с [этим постом](https://www.reddit.com/r/Monero/comments/uny2xi/bounty_to_fix_monero_bounties_site/).

### _Торговля и биржевые спекуляции_

Возможно, декорреляции Monero с другими основными криптовалютами приходит конец.

![28](/img/post/2022-05-26-the-monero-moon-44/28.png)  

Monero вновь пытается выйти из четырёхлетнего нисходящего тренда относительно Bitcoin. Это уже четвёртый раз за последние шесть недель. Ещё ни одной монете не удавалось сделать это в случае с BTC после такого долгого срока. Если же это произойдёт и Monero удастся подняться, можно будет говорить о бычьей тенденции.

![29](/img/post/2022-05-26-the-monero-moon-44/29.png)  

Cointelegraph опубликовал статью под названием «[Топ-3 криптовалют, которые лучше всего справляются с медвежьим рынком в 2022 году](https://cointelegraph.com/news/top-3-cryptocurrencies-that-are-faring-the-best-in-the-2022-bear-market)».

![30](/img/post/2022-05-26-the-monero-moon-44/30.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 126 147 XMR
- Общая рыночная капитализация Monero: 3 353 045.703 USD
- Позиция в рейтенге Coinmarketcap: 25
- Цена XMR/USD: ~195 USD
- Цена XMR/BTC: 0.00661 BTC
- Цена на LocalMonero.co: 209 USD
- Средний размер комиссии за проведение транзакции: 0.000097 XMR ($0.019)
- Хешрейт: 2.634 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![31](/img/post/2022-05-26-the-monero-moon-44/31.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

{{< youtube id="2ofpaF5pkE8" autoplay="false" >}}  

![32](/img/post/2022-05-26-the-monero-moon-44/32.png)  
*Cole & Son advert - https://www.reddit.com/r/Monero/comments/uxn50l/cole_son_promotion_has_a_familar_pillow/*

![33](/img/post/2022-05-26-the-monero-moon-44/33.png)  
*https://boards.4channel.org/biz/thread/49130035*

![34](/img/post/2022-05-26-the-monero-moon-44/34.png)  
*https://twitter.com/CypherPunkus/status/1529035016163893248/photo/4*

![35](/img/post/2022-05-26-the-monero-moon-44/35.png)  

![36](/img/post/2022-05-26-the-monero-moon-44/36.png)  

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 44)](https://www.themoneromoon.com/p/the-monero-moon-issue-44?s=r)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
