---
title: "The Monero Moon (выпуск 40)"
date: "2022-04-28"
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

Как уже говорилось в предыдущем выпуске, обновление сети Monero (хардфорк) запланировано на 16 июля 2022 года на высоте блока 2 668 888. Это согласованное сообществом Monero обновление, которое позволит повысить уровень приватности и производительность сети Monero, а также потребует, чтобы все пользователи обновили своё программное обеспечение. Новая версия v0.18 Fluorine Fermi будет опубликована за месяц до самого обновления, примерно 16 июня. В рамках обновления будет реализован целый ряд новых свойств, таких как:
- размер кольца увеличится с 11 до 16, что повысит уровень приватности;
- будут реализованы теги просмотра, после чего время синхронизации сократится примерно на 40%;
- в результате обновления протокола до версии Bulletproofs+ размер транзакций сократится примерно на 7% и на столько же повысятся показатели верификации.

Полный список улучшений будет опубликован вместе с новой версией программного обеспечения. Если вы хотите больше узнать о грядущем обновлении сети Monero, ознакомьтесь с этим [постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html), опубликованном на официальном [веб-сайте Monero](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html). Вы также можете прочитать [протокол встречи](https://github.com/monero-project/meta/issues/684) разработчиков Monero, состоявшейся 16 апреля, на которой обсуждалось обновление сети.

![01](/img/post/2022-04-28-the-monero-moon-40/01.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*

Официальная версия CLI-кошелька [Monero v0.17.3.2 Oxygen Orion](https://github.com/monero-project/monero/releases/tag/v0.17.3.2) получила тег, и уже скоро можно ожидать публикации двоичных файлов. GUI-версия также получит тег в ближайшее время. Выражаем [Monero Observer](https://www.monero.observer/monero-cli-v0.17.3.2-tagged/) благодарность за эту новость!

![02](/img/post/2022-04-28-the-monero-moon-40/02.png)  
*https://www.monero.observer/monero-cli-v0.17.3.2-tagged/*

В марте 2022 Monero стала самым используемым приватным блокчейн-инструментом. Zcash и Samurai оказались примерно на 99% менее приватными, чем Monero.

![03](/img/post/2022-04-28-the-monero-moon-40/03.png)  

![04](/img/post/2022-04-28-the-monero-moon-40/04.png)

*Визуальное представление количества транзакций Monero в сравнении с другими криптовалютами.*

Говоря о транзакциях Monero, следует упомянуть, что чем больше людей пользуются Monero, тем дешевле это обходится!

![05](/img/post/2022-04-28-the-monero-moon-40/05.png)  

[UnstoppableSwap](https://unstoppableswap.net/), обменный сервис, позволяющий без каких-либо доверенных настроек совершать атомные свопы Bitcoin-Monero, поделился [демонстрационной версией](https://www.reddit.com/r/Monero/comments/uawipv/atomic_swap_gui_demo_on_mainnet_unstoppableswap/) GUI для атомных свопов в основной сети Monero.

![06](/img/post/2022-04-28-the-monero-moon-40/06.png)  
*https://www.reddit.com/r/Monero/comments/uawipv/atomic_swap_gui_demo_on_mainnet_unstoppableswap/*

Если у вас имеется сразу несколько кошельков, в каждом из которых хранится небольшая сумма XMR, то специально для вас [benevanoff](https://github.com/benevanoff/xmr-multisweeper) создал инструмент под названием XMR-Multisweeper. XMR-Multisweeper сканирует блокчейн Monero, выискивая имеющиеся у вас выходы транзакций, которые можно расшифровать, и собирает их в один выбранный вами кошелёк, по сути, объединяя несколько кошельков в один. Следует отметить, что на данный момент это лишь бета-версия. Более подробную информацию и ссылки для скачивания можно найти [здесь](https://github.com/benevanoff/xmr-multisweeper).

![07](/img/post/2022-04-28-the-monero-moon-40/07.png)  
*https://github.com/benevanoff/xmr-multisweeper*

[emesik](https://github.com/monero-ecosystem/monero-python) объявил о необходимости срочного обновления защиты модуля monero-python. Пожалуйста, как можно быстрее обновите его до версии 1.0.2. Более ранние версии уязвимы к атаке, при которой злоумышленник предварительно подделывает транзакцию и проталкивает произвольную сумму платежа, которую код считает действительной. Обновление можно скачать по [этой ссылке](https://github.com/monero-ecosystem/monero-python).

Хотите помочь Monero? Настоятельно рекомендуем создать и использовать собственный узел или заняться майнингом, так как это способствует защите сети. Также возможен соло-майнинг с помощью официального GUI-кошелька Monero, который можно скачать [здесь](https://www.getmonero.org/downloads/), или в пуле, присоединившись к децентрализованному и не требующему разрешений пулу [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html).

![08](/img/post/2022-04-28-the-monero-moon-40/08.png)  
*GlitchPhoenix98 занимается майнингом! - https://www.reddit.com/r/Monero/comments/ubfdsi/im_solo_mining_on_my_cpu_and_mining_in_a_pool_on/*

Если вам интересно, что означает создание и запуск собственного узла, зачем это нужно в принципе и как это сделать, обязательно посмотрите это новое видео из серии Monero Guides.

{{< youtube id="XonyYxjjfcg" autoplay="false" >}}  

Интересуетесь, насколько децентрализована Monero с точки зрения количества и местоположения узлов, работающих по всему миру? Посетите [Monero.fail](https://monero.fail/). По данным этого ресурса, в сети наблюдается более 11 000 узлов. Это далеко не полное представление всей сети Monero, а лишь обзор одноранговых узлов, которые увидел исходный узел (singapore.node.xmr.pm).

![09](/img/post/2022-04-28-the-monero-moon-40/09.png)  
*https://monero.fail/map*

Ознакомьтесь с этой инфографикой, опубликованной [btcMike](https://www.reddit.com/r/Monero/comments/u8e5yr/satoshi_nakamoto_talked_about_privacy_features/) и характеризующей механизмы обеспечения приватности, реализованные Monero, но отсутствующие у Bitcoin.

![10](/img/post/2022-04-28-the-monero-moon-40/10.png)  
*https://www.reddit.com/r/Monero/comments/u8e5yr/satoshi_nakamoto_talked_about_privacy_features/*

### _Прочие новости_

На этой неделе в сообществе Monero возникли некоторые разногласия. Это случилось после того, как децентрализованная биржа Haveno, недавно получившая от сообщества Monero посредством системы общественного финансирования CCS средства на разработку, объявила, что будет поддерживать торговлю Zcash (то есть поддержку торговой пары XMR-ZEC). Такое заявление Haveno по целому ряду причин вызвало негативную реакцию со стороны многих членов сообщества Monero, в то время как другие члены сообщества, наоборот, озвучили свои аргументы в пользу решения Haveno. Если вы хотите спуститься в кроличью нору возникших противоречий, ознакомьтесь с [этим постом](https://www.reddit.com/r/Monero/comments/uaqx9u/haveno_funded_by_the_monero_community_will_list/), опубликованным на Reddit, и [этим твитом](https://twitter.com/HavenoDEX/status/1518121318096461825) от Haveno.

Monero Guides опубликовали свою серию видео Monero под названием «Решительно берёмся за Monero» (Getting to Grips with Monero). Серия включает четыре разных видео, в которых рассматриваются все важные темы, начиная с создания собственного узла и заканчивая совершением первой покупки с помощью Monero. Видео можно посмотреть [здесь](https://www.youtube.com/playlist?list=PLcyDcJ4lpDVBpsnI-fbkB-7O4M63VIA2g) на YouTube или [здесь](https://odysee.com/@moneroguides/01) на Odysee.

![11](/img/post/2022-04-28-the-monero-moon-40/11.png)  
*https://www.youtube.com/channel/UCWeGibnI0h07pIPiX945DBg*

Рагнар Лифтасир (Ragnar Lifthasir), известный почитатель Bitcoin, опубликовал пост под названием «Тайные поклонники Bitcoin, использующие Monero — выход из тени» (Secret Bitcoiner Users of Monero – Come Out Of The Shadows). В своём посте Рагнар призывает сторонников Bitcoin публично поддержать Monero.

![12](/img/post/2022-04-28-the-monero-moon-40/12.png)  

В дополнение к этому Cake Wallet обнаружили, что во время конференции Bitcoin в Майами большинство пользователей предпочитали принимать оплату в Monero, а не в Bitcoin!

![13](/img/post/2022-04-28-the-monero-moon-40/13.png)  

[Monero Talk](https://www.youtube.com/channel/UC3Hx81QYLoEQkm3vyl4N4eQ) опубликовали новое видео с членом сообщества Monero, выступающим под псевдонимом dMartian. dMartian поделился своим видением децентрализованного мира, где Monero может стать инструментом децентрализованного человеческого сотрудничества, который заменит централизованные корпорации и правительства, обладающие всей полнотой власти. Видео можно посмотреть [здесь](https://www.youtube.com/watch?v=7_3PtyruEYc) или ниже.

{{< youtube id="7_3PtyruEYc" autoplay="false" >}}  

Команда Monero Talk также опубликовали видео с конференции Monerotopia с участием Марты Буэно (Martha Bueno), кандидатом на пост мирового судьи округа Майами-Дейд 10, в котором обсудили с ней Monero и приватность финансовой информации.

{{< youtube id="EauJMXqThFk" autoplay="false" >}}  

Вышел [десятый выпуск The Monero Standard](https://localmonero.co/the-monero-standard/weekly/10), в котором освещаются все события за период с 20 по 27 апреля 2022 года. Обязательно ознакомьтесь с ним и оставайтесь в курсе самых последних новостей Monero!

Cointelegraph опубликовали статью под названием «После прорыва нисходящей тенденции наблюдается 75-процентное ралли цены XMR» (Monero ‘falling wedge’ breakout positions XMR price for 75% rally). Найти статью можно [здесь](https://cointelegraph.com/news/monero-falling-wedge-breakout-positions-xmr-price-for-75-rally).

![14](/img/post/2022-04-28-the-monero-moon-40/14.png)  
*https://cointelegraph.com/news/monero-falling-wedge-breakout-positions-xmr-price-for-75-rally*

Coin Bureau разместили новое видео под названием «БЕЗУМНЫЙ отчёт по приватной монете!!! Будет ли она когда-нибудь соответствовать нормам?!» ([CRAZY Privacy Coin Report!! Can They Be Compliant?!?](https://www.youtube.com/watch?v=EIwsMidCk0w)) Несмотря на некоторую ироничность названия, видео довольно серьёзное, и в нём говорится об отчёте Perkin Coies под названием «Регулирование борьбы с отмыванием денег с помощью приватных криптовалют» (Anti-Money Laundering Regulation of Privacy-Enabling Cryptocurrencies). Начиная примерно с 2:40 в видео много говорится о Monero.

{{< youtube id="EIwsMidCk0w" autoplay="false" >}}  

Coin Bureau также намекают на скорый выход видео, посвящённого Monero!

![15](/img/post/2022-04-28-the-monero-moon-40/15.png)  

Ирина Хивер ([Irina Heaver](https://youtu.be/AlRBZm61D-M?t=1495)), генеральный партнер Ikigai Ventures и юрист по профессии, выступила на Парижском саммите по блокчейн-технологии по вопросу юридических и моральных последствий выпуска CBDC, то есть цифровых валют, создаваемых центральными банками. В выступлении была затронута тема необходимости приватности финансовой информации, а также говорилось о том, что приватность является вовсе не преступлением, а неотъемлемым правом человека. О Monero было сказано примерно [на 24-й минуте](https://youtu.be/AlRBZm61D-M?t=1495) выступления. Видео можно посмотреть ниже.

{{< youtube id="AlRBZm61D-M" autoplay="false" >}}  

Комик Рассел Брэнд (Russell Brand), ставший политическим активистом, опубликовал очередное видео, предупреждающее об опасности отслеживаемых CBDC и криптовалют. Получилось на удивление информативное и занимательное видео.

{{< youtube id="tzIPJfqFETU" autoplay="false" >}}  

[Son of a Tech](https://www.themoneromoon.com/p/the-monero-moon-issue-40?s=r), ютубер, у которого уже есть более 100 тысяч подписчиков, опубликовал видео о предстоящем хардфорке Monero, которое можно посмотреть ниже.

{{< youtube id="dVr867AC9fA" autoplay="false" >}}  

### _Мероприятия_

Встреча [Исследовательской лаборатории Monero](https://github.com/monero-project/meta/issues/697) запланирована на 27 апреля 2022 года и состоится в 17:00 UTC на IRC-канале #monero-research-lab.

![16](/img/post/2022-04-28-the-monero-moon-40/16.png)  
*https://github.com/monero-project/meta/issues/697*

Встреча [Рабочей группы сообщества Monero](https://github.com/monero-project/meta/issues/695) запланирована на 1 мая 2022 (18:00 UTC) на IRC-канале #monero-community. К участию приглашаются все желающие, даже если вы захотите просто поглазеть.

Очередная плановая встреча по проведению MoneroKon 2022 состоится в субботу, 30 апреля 2022 года в 18:00 UTC на IRC-канале #monero-events.

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Билеты на MoneroKon теперь можно приобрести [здесь](https://monerokon.com/products/monerokon2022), на веб-сайте MoneroKon.

![17](/img/post/2022-04-28-the-monero-moon-40/17.png)  
*https://monerokon.com/*

### _Биржи и предприниматели_

Crypto In Power Out, также известный как Cipo, теперь позволяет оплачивать электроэнергию, потребляемую вашим фургоном для кемпинга, электромобилем, лодкой, домом на колёсах и другими энергоёмкими механизмами, с помощью XMR. Узнать о Cipo больше можно [здесь](https://www.publish0x.com/jonny/meet-cipo-xznknvz) или из видео, размещённого ниже.

![27](/img/post/2022-04-28-the-monero-moon-40/27.png)  
*https://odysee.com/@Cipo:5/First-demo-2022-04-22:6*

VPN-сервис Mullvad скоро позволит оплачивать свои услуги в XMR непосредственно на своём веб-сайте. Более подробную информацию можно найти [здесь](https://www.reddit.com/r/mullvadvpn/comments/ubjeb8/monero_support_will_soon_be_added_to_mullvad/).

![18](/img/post/2022-04-28-the-monero-moon-40/18.png)  
*https://www.reddit.com/r/mullvadvpn/comments/ubjeb8/monero_support_will_soon_be_added_to_mullvad/*

MoneroDirectory.com в настоящее время выставлен на продажу примерно за 10-15 XMR. Monero Directory — это сайт, на котором можно найти самые разные сервисы и веб-сайты, принимающие Monero в качестве оплаты.

![19](/img/post/2022-04-28-the-monero-moon-40/19.png)  
*https://monerodirectory.com/*

Веб-сайт Monero.com был обновлен и дополнен множеством новых интересных функций!

![20](/img/post/2022-04-28-the-monero-moon-40/20.png)  

В связи с этим Cake Wallet недавно удалили свой кошелёк Monero.com из Google Play Store, поскольку значок приложения был похож на Freewallet (кошелек, не рекомендуемый к использованию сообществом Monero). Дополнительную информацию по этому вопросу можно найти в [данном посте](https://www.reddit.com/r/Monero/comments/u8rxr0/google_has_removed_monerocom_from_the_play_store/).

![21](/img/post/2022-04-28-the-monero-moon-40/21.png)  

Также в связи с Freewallet один из пользователей Monero сделал заявление, согласно которому с октября 2020 года Freewallet неправомерно удерживал его 365 XMR. После отправления примерно 150 электронных писем в Freewallet пользователь Monero [istvanx](https://www.reddit.com/r/Monero/comments/ual81s/36504_montero_wrongfully_withheld_since_october/) теперь утверждает, что «нанял адвокатов в Гонконге, откуда якобы и работают «Wallet Services Limted», они же Freewallet. Адвокаты отправили кого-то в «штаб-квартиру Freewallet», чтобы лично вручить исковое письмо, но, к сожалению, в указанном месте не оказалось никаких офисов».

Waves.Exchange объявили о планах прекратить поддержку Monero и других «приватных монет».

![22](/img/post/2022-04-28-the-monero-moon-40/22.png)  

После мероприятия Monerun, в рамках которого пользователи Monero скоординировано выводили свои XMR с бирж, gr8ful4 опубликовал пост, в котором были перечислены те криптовалютные биржи, которые предположительно используют схемы частичного резервирования. Хотя это и может оказаться правдой, всё же неясно, как составлялся этот список. Подробнее об этом читайте [здесь](https://www.reddit.com/r/Monero/comments/u8uofv/after_the_monerorun_is_before_the_monerorun/).

![23](/img/post/2022-04-28-the-monero-moon-40/23.png)  
*https://www.reddit.com/r/Monero/comments/u8uofv/after_the_monerorun_is_before_the_monerorun/*

Хотите принимать XMR в качестве оплаты, не являясь техническим специалистом? [ozc1han](https://www.reddit.com/r/Monero/comments/u8t9vo/accepting_monero_as_a_merchant_in_aus_pt2/) поделился коротким видео, в котором предлагается несколько рудиментарный, но простой способ, воспользовавшись которым вы сможете реализовать своё желание. Рассчитайте сумму XMR в фиатной валюте, а затем перенесите её в кошелёк и получите оплату.

![24](/img/post/2022-04-28-the-monero-moon-40/24.png)  
*https://www.reddit.com/r/Monero/comments/u8t9vo/accepting_monero_as_a_merchant_in_aus_pt2/*

Если у вас возникли проблемы, связанные с соответствующим программным обеспечением Monero или криптовалютными биржами, пожалуйста, будьте осторожны с теми, кто утверждает, что работает в «службе поддержки». Никогда не отправляйте пароли или мнемонические фразы Monero кому бы то ни было, независимо от характера возникшей проблемы, и не переходите по ссылкам, которые вам приходят от посторонних людей.

![25](/img/post/2022-04-28-the-monero-moon-40/25.png)  
*Вот пример мошенничества, осуществляемого под видом службы поддержки - https://www.reddit.com/r/Monero/comments/ucczoo/this_seems_like_a_scam/*

Вы можете воспользоваться [этими изображениями](https://www.reddit.com/r/Monero/comments/ubtu7q/free_monero_stickersposters/) от Odd_Error_, чтобы создать собственные плакаты или стикеры.

![26](/img/post/2022-04-28-the-monero-moon-40/26.png)  
*https://www.reddit.com/r/Monero/comments/ubtu7q/free_monero_stickersposters/*

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![28](/img/post/2022-04-28-the-monero-moon-40/28.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![29](/img/post/2022-04-28-the-monero-moon-40/29.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![30](/img/post/2022-04-28-the-monero-moon-40/30.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

После двухмесячного восходящего тренда невероятный рост Monero столкнулся со встречным ветром.

Недельный график XMR/BTC свидетельствует об изменении цены ниже уровня сопротивления/поддержки четырёхлетней давности, хот до этого цена шла вверх. В идеале быкам хотелось бы, чтобы недельные и месячные свечи закрылись выше жёлтой линии, продолжив соответствующий тренд.

![31](/img/post/2022-04-28-the-monero-moon-40/31.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 113 636 XMR
- Общая рыночная капитализация Monero: 4 263 827.042 USD
- Позиция в рейтенге Coinmarketcap: 34
- Цена XMR/USD: 233 USD
- Цена XMR/BTC: 0,00592 BTC
- Цена на LocalMonero.co: 245 USD
- Средний размер комиссии за проведение транзакции: 0.0001 XMR ($0.024)
- Хешрейт: 2.813 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![32](/img/post/2022-04-21-the-monero-moon-39/32.png)  
_https://minexmr.com/pools.html_

### _Для развлечения_

![33](/img/post/2022-04-28-the-monero-moon-40/33.png)  
twitter.com/DontTraceMeBruh/status/1518536845302317057/photo/1*

![34](/img/post/2022-04-28-the-monero-moon-40/34.png)  
*https://www.reddit.com/user/afsdkjhblkjhbav/comments/ucq1f8/privacy_is_king/*

![35](/img/post/2022-04-28-the-monero-moon-40/35.png)  
*https://boards.4channel.org/biz/thread/48285190*

![36](/img/post/2022-04-28-the-monero-moon-40/36.png)  
*https://boards.4channel.org/biz/thread/48285190*

![37](/img/post/2022-04-28-the-monero-moon-40/37.png)  
*https://www.reddit.com/r/Monero/comments/u9hilb/there_was_a_roundnet_easter_tournament_in_my_city/*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 40)](https://www.themoneromoon.com/p/the-monero-moon-issue-40)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
