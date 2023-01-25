---
title: "The Monero Moon (выпуск 61)"
date: "2023-01-24"
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

[Rucknium](https://www.reddit.com/user/Rucknium/), член [Исследовательской лаборатории Monero](https://www.getmonero.org/resources/research-lab/), сообщил, что некоторые централизованные майнинг-пулы в среднем задерживают первое подтверждение транзакций Monero на целую минуту. Быстрее всех остальных транзакции добавлялись в блоки децентрализованным пулом P2Pool. Согласно опубликованным Rucknium результатам исследования, пулы HashVault и MoneroOcean изменили свою конфигурацию так, чтобы их шаблоны блоков обновлялись чаще. Более подробную информацию можно найти в [блоге Rucknium](https://rucknium.me/posts/monero-pool-transaction-delay/) и [посте](https://www.reddit.com/r/Monero/comments/10gapp9/centralized_mining_pools_are_delaying_monero/), опубликованном на Reddit.

![01](/img/post/2023-01-24-the-monero-moon-61/01.png)  
*https://rucknium.me/posts/monero-pool-transaction-delay/*

[Monero Time](https://twitter.com/MoneroTime/) создали в Twitter [ветку](https://twitter.com/MoneroTime/status/1617536536358322176?s=20), посвящённую обновлению [Seraphis и Jamtis](https://github.com/seraphis-migration/strategy/wiki/Seraphis-and-Jamtis-Resources), которое должно состояться в 2024 году. Seraphis — это протокол транзакций следующего поколения, в рамках которого были реализованы все знания, накопленные за последние десять лет, начиная с появления CryptoNote. Об этом подробно рассказал [Джастин Берман в своём выступлении](https://www.youtube.com/watch?v=xGEBRQU1lzw) на Monerokon 2022. Исчерпывающую информацию, связанную с Seraphis  и Jamtis, можно найти [здесь](https://github.com/seraphis-migration/strategy/wiki/Seraphis-and-Jamtis-Resources).

![02](/img/post/2023-01-24-the-monero-moon-61/02.png)  

{{< youtube id="ipUoSEV94N4" autoplay="false" >}}  

[binarybaron](https://github.com/binarybaron/) опубликовал [UnstoppableSwap GUI v0.4.6](https://monero.observer/binarybaron-releases-unstoppable-swap-gui-v0.4.6/). В очередной версии появилась пара новых функций, а также, например, добавлены всплывающие подсказки для провайдеров свопов. Более подробно об этом рассказано [здесь](https://github.com/UnstoppableSwap/unstoppableswap-gui/releases/). А ниже предлагается видео, демонстрирующее, как производятся атомные свопы с помощью [UnstoppableSwap](https://unstoppableswap.net/).

{{< youtube id="xGEBRQU1lzw" autoplay="false" >}}  

Команда [The Farcaster Project](https://github.com/farcaster-project/) выложила в доступ [версию 0.8.4](https://github.com/farcaster-project/farcaster-node/releases) узла Farcaster, позволяющего совершать атомные свопы между блокчейнами. Создайте свой узел и с помощью [браузерного GUI](https://farcaster.dev/) войдите в тестовую сеть Farcaster для проведения атомных свопов XMR-BTC. Также рекомендуется посетить страницу проекта на [GitHub](https://github.com/farcaster-project/farcaster-node/releases) или ознакомиться с [этим постом](https://www.reddit.com/r/Monero/comments/10dp1mw/farcaster_atomic_swap_node_gui_mvp_release/) на Reddit, где обо всём рассказано более подробно.

![03](/img/post/2023-01-24-the-monero-moon-61/03.png)  
*https://farcaster.dev/*

[Elite Labs](https://github.com/Elite-Labs) выпустили [Elite Wallet](http://ttps/elitewallet.sc/), бесплатный, ориентированный на обеспечение приватности кошелёк с открытым исходным кодом, поддерживающий сразу множество валют. Доступны версии для iOS и Android. Это некастодиальный, не требующий размещения на сервере кошелёк, использующий проверенные узлы сообщества, который, помимо прочего, имеет встроенную функцию обмена валют. Вы также можете купить XMR непосредственно в приложении с помощью своей дебетовой или кредитной карты, а также продать криптовалюту посредством банковского перевода. При этом некоторые члены сообщества [отметили](https://monero.observer/elite-technologies-announces-elitewallet/), что это форк Cake Wallet с удалённой историей коммитов, а также, что кошелёк берёт данные цены на CoinGecko. Кошелёк можно скачать на Google Play Store или просто как приложение APK. В скором времени планируется выпуск десктоп-версии. Всю дополнительную информацию можно найти [здесь](https://github.com/Elite-Labs/EliteWallet) и [здесь](https://www.reddit.com/r/Monero/comments/10aa3pc/elitewallet_free_and_opensource_multicurrency/).

![04](/img/post/2023-01-24-the-monero-moon-61/04.png)  
*https://elitewallet.sc/*

Вышла [версия v2.2.3](https://featherwallet.org/download/) бесплатного кошелька [Feather Wallet](https://featherwallet.org/) с открытым исходным кодом, реализованным в стиле Electrum. Была решена проблема с невозможностью подключения кошелька к устройствам Trezor под macOS. Также была опубликована версия v2.2.2, содержащая ещё большие усовершенствований. К тому же у версий Feather Wallet теперь появилась функция [самостоятельной загрузки и настройки](http://bootstrappable.org/), то есть все их элементы и зависимости будут строиться автоматически на основе исходного кода. Последняя версия поддерживает Raspberry Pi и Linux ARM64, а сборки macOS теперь предлагаются в виде файла .dmg. Подробную информацию о прочих улучшениях Feather Wallet можно найти [здесь](https://featherwallet.org/changelog/), а сама новая версия доступна для скачивания по [этой ссылке](https://featherwallet.org/download/).

![05](/img/post/2023-01-24-the-monero-moon-61/05.png)  
*https://featherwallet.org/changelog/*

[Monerujo](https://www.monerujo.io/), Android-кошелёк Monero, поддерживающий аппаратный кошелёк Ledger, был обновлён до [версии v3.1.0](https://github.com/m2049r/xmrwallet/releases/tag/v3.1.0). Теперь вы сможете увидеть, если получите заблокированную транзакцию. Прочие подробности были изложены в [этом твите](https://twitter.com/monerujowallet/status/1611881463804313604?s=20). Скачать обновление можно [здесь](https://www.monerujo.io/).

![06](/img/post/2023-01-24-the-monero-moon-61/06.png)  

Cake Labs выпустили очередные версии Cake Wallet v4.5.6 и Monero.com Wallet v1.2.5. Чтобы узнать, что было изменено, перейдите по [этой ссылке](https://github.com/cake-tech/cake_wallet/releases/tag/v4.5.6).

![07](/img/post/2023-01-24-the-monero-moon-61/07.png)  

Также вышла [версия v1.5.28](https://github.com/cypherstack/stack_wallet/releases/tag/build_102) Stack Wallet. [Stack Wallet](https://stackwallet.com/) — это некастодиальный, обеспечивающий приватность криптовалютный кошелёк с открытым исходным кодом, помимо прочего поддерживающий Monero. Более подробно о новой версии написано [здесь](https://github.com/cypherstack/stack_wallet/releases/tag/build_102) на GitHub.

![08](/img/post/2023-01-24-the-monero-moon-61/08.png)  
*https://github.com/cypherstack/stack_wallet/releases/tag/build_102*

LocalMonero/AgoraDesk выпустили [версию v1.0.49](https://github.com/AgoraDesk-LocalMonero/agoradesk-app-foss/releases) своих мобильных приложений. Были исправлены всевозможные недочёты и добавлены новые функции. Подробности, связанные с новой версией, и ссылки на скачивание можно найти по [этой ссылке](https://github.com/AgoraDesk-LocalMonero/agoradesk-app-foss/releases).

![09](/img/post/2023-01-24-the-monero-moon-61/09.png)  
*https://github.com/AgoraDesk-LocalMonero/agoradesk-app-foss/releases*

[Trocador.app](https://trocador.app/) реализовали Monero Bridge, функцию, ранее известную как Monero Tunnels, позволяющую пользователю совершать сделки между двумя разными блокчейнами. Если у кого-то имеются средства в прозрачном блокчейне, таком как Bitcoin, и он хочет переключиться на другой прозрачный блокчейн, такой как Ethereum, Trocador.app вычислит обменный курс, проведя средства через Monero между двумя различными биржами, повысив таким образом ликвидность. Сервис изначально задумывался как способ повышения анонимности кошельков. Однако после обсуждения вопроса сообществом было принято решение, что свойства сервиса, связанные с приватностью, ограничены и первичным его преимуществом является способность повысить ликвидность. Подробнее о Monero Bridge (Monero Tunnels) можно прочитать [здесь](https://www.reddit.com/r/Monero/comments/10fcjdr/using_monero_tunnels_for_swaps_between_two/).

![10](/img/post/2023-01-24-the-monero-moon-61/10.png)  
*https://trocador.app*

Команда, стоящая за разработкой и сопровождением биржевого агрегатора [Trocador.app](https://trocador.app/) также создала новый плагин для сервера BTCPay, который позволяет принимать Monero. Кроме того, плагин работает при отключённом JavaScript и помимо прочего, например, позволяет клиентам расплачиваться любой валютой через Trocador, настраивается в соответствии с цветами магазина, позволяет создавать профили платежей в фиатных валютах и менять названия платёжных методов. Больше о новом плагине можно узнать по [этой ссылке](https://www.reddit.com/r/Monero/comments/10gyi70/new_btcpay_server_plugin_that_accepts_monero_and/).

![11](/img/post/2023-01-24-the-monero-moon-61/11.png)  
*https://www.reddit.com/r/Monero/comments/10gyi70/new_btcpay_server_plugin_that_accepts_monero_and/*

Команда Monero ATM Project, работающая над созданием собственного банковского автомата, использующего свободное программное обеспечение, объявила, что проект может быть завершён к моменту проведения MoneroKon 2023. Согласно информации, опубликованной Monero Observer, участники проекта «уже получили большую часть деталей, включая купюроприёмник из Румынии»! Более подробно обо всём рассказывается в [этом посте](https://monero.observer/the-monero-atm-project-could-be-completed-before-monerokon23/) и на [веб-сайте проекта](https://atm.monero.is/).

![12](/img/post/2023-01-24-the-monero-moon-61/12.png)  
*https://atm.monero.is/*

[Ora_pro_vivis](https://www.reddit.com/user/Ora_pro_vivis/), разработчик [POS-приложения с открытым исходным кодом для Monero](https://www.reddit.com/r/Monero/comments/10j8pdf/update_merchant_a_foss_desktop_point_of_sale_app/), объявил, что разработка по-прежнему продолжается и выход альфа-версии задерживается. Также было сообщено официальное название проекта — [Kasejo](https://kasejo.com/), что на языке эсперанто означает «выписка чека». Также планируется провести [конкурс на создание логотипа](https://www.reddit.com/r/Monero/comments/10j8pdf/update_merchant_a_foss_desktop_point_of_sale_app/), победитель которого получит приз в Monero. Кроме того, Ora_pro_vivis купил ещё одно доменное имя, [rezisto.net](https://rezisto.net/), для хранения кода и другого связанного с проектом контента. Наконец, было объявлено о запуске Lumo, сервера Node JS, позволяющего самостоятельно разместить полупрозрачный, предусматривающий возможность аудита кошелёк Monero для сбора пожертвований в благотворительных целях. Все желающие приглашаются к тестированию. С подробностями можно ознакомиться [здесь](https://www.reddit.com/r/Monero/comments/10j8pdf/update_merchant_a_foss_desktop_point_of_sale_app/).

![13](/img/post/2023-01-24-the-monero-moon-61/13.png)  
*https://kasejo.com/*

Обновление (хардфорк) майнинг-пула P2Pool в соответствии с новыми правилами консенсуса состоится 18 марта 2023, в 21:00 UTC. Со слов разработчика P2Pool [SChernykh](https://www.reddit.com/r/MoneroMining/comments/1095730/psa_p2pool_network_upgrade_aka_hardfork_on_march/), «хардфорк необходим для повышения масштабируемости P2Pool и снижения его влияния на блокчейн Monero». Если вы пользуетесь P2Pool, вам будет необходимо обновить его до версии v3.0 или до более новой версии. Всю имеющуюся информацию можно найти по [этой ссылке](https://www.reddit.com/r/MoneroMining/comments/1095730/psa_p2pool_network_upgrade_aka_hardfork_on_march/). Обновление можно обсудить в [соответствующей ветке](https://twitter.com/hundehausen/status/1613285401359417346?s=20) в Twitter.

![14](/img/post/2023-01-24-the-monero-moon-61/14.png)  

Также всем настоятельно рекомендуется создать и поддерживать собственный узел — это способствует повышению уровня безопасности сети Monero. Также можно заняться соло-майнингом с помощью официального GUI-кошелька Monero, который можно [скачать здесь](https://www.getmonero.org/downloads/), или же воспользовавшись децентрализованным и не требующим каких-либо разрешений пулом [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html). Официальный веб-сайт Monero [getmonero.org](https://www.getmonero.org/get-started/mining/) или сайт [sethforprivacy.com](https://sethforprivacy.com/guides/) также помогут вам создать и запустить узел или заняться майнингом.

![15](/img/post/2023-01-24-the-monero-moon-61/15.png)  
*https://p2pool.io/#pool*

В следующем видео от [CryptoCasts](https://www.youtube.com/watch?v=ipUoSEV94N4) показано, как установить и подсоединиться к собственному узлу Monero с помощью приложений в macOS X Monterrey и iOS Cake Wallet на iPhone.

{{< youtube id="ipUoSEV94N4" autoplay="false" >}}  

Благодаря [XMRig](https://github.com/XMRig-for-Android/xmrig-for-android) вы можете заниматься майнингом даже с помощью устройства на базе Android. В этом вам поможет это обучающее видео от [Cursed Mining](https://www.youtube.com/watch?v=Oco_3rGVaQo).

{{< youtube id="Oco_3rGVaQo" autoplay="false" >}}  

За последние сутки в сети Monero наблюдалось более 11 тыс. узлов. Для сравнения: в сети Ethereum также присутствует [примерно 11 тыс. активных узлов](https://etherscan.io/nodetracker).

![16](/img/post/2023-01-24-the-monero-moon-61/16.png)  
*https://monero.fail/map*

[dsmlegend](https://gitlab.com/dsmlegend) ждёт отзыва со стороны сообщества на сценарии серии новых анимационных видео, посвящённых продвижению Monero. С этими сценариями можно ознакомиться на [Gitlab](https://gitlab.com/monero-videos/monero-adoption-animated-videos/) или в [субреддите Monero](https://www.reddit.com/r/Monero/comments/10j3gn5/monero_animated_series_final_review/), а обсуждаются они [здесь](https://www.reddit.com/r/Monero/comments/10j3gn5/monero_animated_series_final_review/).

![17](/img/post/2023-01-24-the-monero-moon-61/17.png)  
*https://gitlab.com/monero-videos/monero-adoption-animated-videos/-/blob/main/Video%202%20Script.md*

Разработчик Monerujo [anhdres](https://repo.getmonero.org/anhdres) поделился [отчётом](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/346) по продвижению работы над новым проектом [Monero Garden](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/346), который пишется им с помощью ELI5 и по задумке должен стать удобным источником информации для новых (и не только) членов сообщества Monero.

![18](/img/post/2023-01-24-the-monero-moon-61/18.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/346*

Хотите создать фальшивый кошелёк Monero и получить таким образом «магический щит» для защиты мнемонической фразы вашего кошелька от атак Evil Maid? [Monero Observer](https://monero.observer/cypherpunk-transmission-011-decoy-wallets-seed-offset-passphrase-monero-cli/) опубликовали короткое руководство, которое поможет вам создать фальшивый кошелёк XMR, воспользовавшись CLI-кошельком.

![19](/img/post/2023-01-24-the-monero-moon-61/19.png)  
*https://monero.observer/cypherpunk-transmission-011-decoy-wallets-seed-offset-passphrase-monero-cli/*

[Monero Observer](https://monero.observer/cypherpunk-transmission-011-decoy-wallets-seed-offset-passphrase-monero-cli/) также опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-3-2023/).

![20](/img/post/2023-01-24-the-monero-moon-61/20.png)  
*https://monero.observer/monero-dev-activity-report-week-3-2023/*

### _Прочие новости_

Ждём выхода новой книги под названием The Monero Standard. Список глав уже опубликован, и, согласно размещённой на веб-сайте информации, книга будет о том, «как можно воспользоваться деньгами, чтобы фундаментально, революционно изменить систему мотивации общества, о том, с какими вызовами сталкивается это общество сегодня, и как им противостоять, чтобы в итоге создать долговечную платформу, которая обеспечит всем свободу и процветание». Цифровую и твёрдую копии книги можно заказать уже сегодня на [MoneroStandard.com](http://monerostandard.com/).

![21](/img/post/2023-01-24-the-monero-moon-61/21.png)  

[Вик Шарма](https://twitter.com/vikrantnyc), основатель [Cake Wallet](https://twitter.com/cakewallet), опубликовал [пост](https://www.reddit.com/r/Monero/comments/10f7qrs/cake_wallet_the_5_year_journey/), в котором подробно описывается путь проекта за прошедшие пять лет. Очень интересный материал. Вы сможете узнать всё с самого начала и насколько продвинулась команда Cake Wallet с момента запуска проекта.

![22](/img/post/2023-01-24-the-monero-moon-61/22.png)  
*https://www.reddit.com/r/Monero/comments/10f7qrs/cake_wallet_the_5_year_journey/*

[Monero Magazine](https://www.youtube.com/watch?v=Ze6KBC15w78) взяли интервью у ютубера Люка Смита. Обсуждался самый широкий диапазон тем, включая глобализм, свободу и роль Monero в формировании будущего.

https://youtu.be/JvLbiZiBowk

Также Monero Magazine встретились с Рафаэлем Лаверде, с которым поговорили о роли Monero как цифровой валюты в обществе. Видео можно найти по [этой ссылке](https://www.youtube.com/watch?v=WQSuDkcnWPE).

{{< youtube id="WQSuDkcnWPE" autoplay="false" >}}  

Monero Talk выпустили [сотый «живой» эпизод Monerotopia](https://www.youtube.com/watch?v=hEx2OiZr4KE). В нём канал поделился новостями, связанными с организацией Monerotopia 2023, представил отчёт по ценам от [BawdyAnarchist](https://twitter.com/BawdyAnarchist_), а также принял специального гостя, Элиана из Decred Project.

{{< youtube id="hEx2OiZr4KE" autoplay="false" >}}  

Появился новый, посвящённый Monero субреддит — [r/MoneroMeansMoney](https://www.reddit.com/r/MoneroMeansMoney/). Модератором субреддита является [bawdyanarchist](https://www.reddit.com/user/bawdyanarchist/) и со слов создателей, это будет место обсуждения «[сторонних, противоречивых и запретных тем членами сообщества Monero](https://www.reddit.com/r/Monero/comments/10by3w6/an_outlet_for_offtopic_controversial_and_taboo/)». И если вас волнует какая-то неудобная тема, связанная с Monero, и вы хотели бы поделиться своим мнением, то новый форум — именно то, что вам нужно.

![23](/img/post/2023-01-24-the-monero-moon-61/23.png)  
*https://www.reddit.com/r/MoneroMeansMoney/*

Для тех, кто уже состоит или только собирается присоединиться к сообществу Monero на XMPP, сообщаем, что адрес хоста [поменялся](https://www.reddit.com/r/Monero/comments/10hm6hf/community_xmpp_server_change/) на [monero@chat.yax.im](http://monero@chat.yax.im/).

Опубликован 37-й выпуск новостного дайджеста [The Monero Standard](https://localmonero.co/the-monero-standard/). Ознакомившись с ним, вы будете в курсе самых последних новостей Monero!

Также был опубликован 155-й выпуск Revuo Monero. [Revuo Monero](https://revuo-xmr.com/) — это всегда свежая недельная доза новостей, связанных с Monero!

![24](/img/post/2023-01-24-the-monero-moon-61/24.png)  

Monero упоминается в сериале Netflix «[Исчезновение в Лёренскуге](https://www.imdb.com/title/tt15264452/)».

![25](/img/post/2023-01-24-the-monero-moon-61/25.png)  

Состоялись [выборы членов комитета](https://magicgrants.org/Monero-Fund-2023-Election-Results/) MAGIC Monero Fund 2023 года. Три новых члена комитета фонда были выбраны путём рейтингового голосования. В ближайшие 2 года рядом с Rucknium и kayabaNerve места в комитете будут занимать MajesticBank, monerobull и artlimber. Фонд MAGIC Grants является общественной благотворительной организацией, занимающейся выплатой стипендий студентам, интересующимся Monero и другими криптовалютами, а также поддержкой всевозможной публичной платёжной криптовалютной инфраструктуры.

![26](/img/post/2023-01-24-the-monero-moon-61/26.png)  
*https://magicgrants.org/Monero-Fund-2023-Election-Results/*

Джордж Николас, отмеченный наградами режиссёр и энтузиаст Monero, ранее принявший участие в создании документального фильма [Monero означает «деньги»](https://moneromeans.money/), написал сценарий и режиссировал независимый 38-минутнфый фильм под названием «Отличительный знак». Фильм снимался в Мексике, в городе Тихуана, но Monero не является его основной темой. Monero упоминается в нём как Monero Casascius Coin, а в одной из сцен использовалась песня [Crypt0 Bear](https://twitter.com/Crypt0_Bear). Для выпуска фильма, чтобы он смог принять участие в фестивалях, для его рекламы, найма журналистов для написания положительных отзывов, в целом проведения кампании с целью получения призов, [требуются средства](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/371). Автор попросил помощи у сообщества Monero, а в ответ в титрах фильма будет выражена благодарность в его адрес, что позволит большему количеству людей узнать о Monero. За последние 48 часов соответствующий [запрос в системе CCS](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/371) получил массу откликов. Заходите в CCS и [делитесь своим мнением](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/371).

![27](/img/post/2023-01-24-the-monero-moon-61/27.gif)  

---

![28](/img/post/2023-01-24-the-monero-moon-61/28.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/371*

### _Встречи и мероприятия_

Встреча [Исследовательской лаборатории Monero](https://www.getmonero.org/resources/research-lab/) (MRL) состоится в среду, 25 января, в 17:00 UTC. Соответствующие ссылки и дополнительную информацию о встрече, благодаря Monero Observer, можно найти [здесь](https://monero.observer/monero-research-lab-meeting-25-january-2023/). Встреча лаборатории MRL пройдёт на IRC-канале #monero-research-lab. Заглядывайте, если вам интересно, и увидите всё сами в режиме реального времени.

![29](/img/post/2023-01-24-the-monero-moon-61/29.png)  
*https://www.getmonero.org/resources/research-lab/*

Очередная встреча Рабочей группы по вопросам сообщества запланирована на субботу, 28 января 2023 года, 16:00 UTC, и состоится на IRC-канале #monero-community. Будут обсуждаться новые предложения и новости сообщества и отчёты рабочих групп.

Следующая встреча Рабочей группы Seraphis запланирована на понедельник, 30 января 2023 года, 18:00 UTC. Все подробности можно найти по [этой ссылке](https://monero.observer/seraphis-wallet-workgroup-meeting-30-january-2023/).

Вторая в истории конференция [Monerotopia](https://monerotopia.com/) пройдёт в Мехико 6-7 мая 2023. Monerotopia — это конференция, где встречаются любители приватности, технологий и свободы. Уже составлен потрясающий список подтверждённых докладчиков, среди которых можно увидеть целый ряд разработчиков и контрибьюторов Monero. Билет на одну из самых горячих конференций Monero можно уже сейчас приобрести на официальном [веб-сайте Monerotopia](https://monerotopia.com/)! Воспользуйтесь промокодом moneromoon8ar и получите скидку в 10%!

![30](/img/post/2023-01-24-the-monero-moon-61/30.png)  

После успешного возвращения [Monero Konferenco](https://twitter.com/monerokon) в 2022 году мероприятие 2023 года пройдет в здании театра [La Fabrika](https://www.lafabrika.cz/en/lafabrika) в Праге, Чешская Республика, 23-25 июня 2023 года. [MoneroKon](http://monerokon.com/) — это ежегодная встреча поборников приватности, шифропанков, учёных и философов, призванная распространить взгляды, а также поделиться научными и техническими результатами в области технологий обеспечения приватности и финансовых технологий, связанными, например, с устойчивыми к цензурированию цифровыми деньгами. Более подробную информацию можно найти [здесь](https://ccs.getmonero.org/proposals/monerokon-2023-ccs-1.html), в предложении по финансированию MoneroKon 2023, размещённому в системе CCS, или непосредственно на [веб-сайте MoneroKon](https://monerokon.com/).

Если вы хотите стать волонтером и помочь на MoneroKon 2023 в обмен на бесплатный билет или просто потому, что любите Monero, вы можете подать заявку, заполнив [соответствующую форму](https://cryptpad.disroot.org/form/#/2/form/view/Z8v7RE0D+Axf+54kTA-otpnJ-Krlfs8gJwoktERKUrM/embed/)!

Следующая планировочная встреча по проведению MoneroKon 2023 пройдёт 28 января 2023 года, в 18:00 UTC, на IRC-канале #monero-events. Более подробную информацию можно найти [здесь](https://github.com/monero-project/meta/issues/771).

![31](/img/post/2023-01-24-the-monero-moon-61/31.png)  
*https://twitter.com/MoneroKon*

### _Биржи и предприниматели_

Хотите купить или продать что-то за XMR? Зайдите на [MoneroMarket.io](https://moneromarket.io/) и ознакомьтесь со списком предлагаемых товаров или добавьте свой. Следует отметить, что некоторые из товаров могут показаться неподобающими. Также сервис предлагает возможность эскроу хранения ваших средств. Обязательно посетите их [веб-сайт](https://moneromarket.io/).

![32](/img/post/2023-01-24-the-monero-moon-61/32.png)  
*https://moneromarket.io*

[AllArk](https://allark.io/) теперь предлагает сервис, позволяющий пользователям перевести XMR в любой банк мира через SWIFT. Лимит перевода составляет 2 миллиона USD. Также с помощью сервиса пользователь может разместить заявку на ту сумму XMR, которую он хочет продать, указать данные депозита, а затем получить средства без каких-либо дополнительных действий и ожидания. Все подробности можно узнать [здесь](https://www.reddit.com/r/Monero/comments/10jcmim/allark_wishes_you_a_great_year_ahead_and_now/).

![33](/img/post/2023-01-24-the-monero-moon-61/33.png)  
*https://allark.io/*

[ShopinBit](https://shopinbit.com/), онлайн-ретейлер, предлагающий скидку в 3%, если вы оплачиваете товар в XMR, добавил новую «модную» категорию товаров, где клиенты смогут выбрать себе одежду, ювелирные украшения, солнечные очки, обувь, а также более 3000 различных моделей часов!

![34](/img/post/2023-01-24-the-monero-moon-61/34.png)  
*https://shopinbit.com/*

Сервис [CryptoPost](https://cryptopost.global/main) позволяет приобрести транспортные этикетки таких популярных перевозчиков, как DHL и USPS, за Monero. CryptoPost при этом собирает только ту информацию, которая необходима для доставки посылки из пункта A в пункт Б, а также чистит всю информацию, имеющуюся на его серверах, каждые 7 дней. Если вас заинтересовало их предложение, просто перейдите по [этой ссылке](https://www.reddit.com/r/Monero/comments/109e3y2/cryptopost_buy_printathome_shipping_labels_with/).

![35](/img/post/2023-01-24-the-monero-moon-61/35.png)  
*https://cryptopost.global/main*

Humane Society of Independence County, приют для животных, расположенный в Бейтсвилле, штат Арканзас, теперь принимает пожертвования в Monero. Если вы хотите помочь приюту, посетите их веб-сайт.

[MoneroSupplies.com](https://monerosupplies.com/) создали эксклюзивную акриловую фигурку Monerchan. Все подробности желающие найдут на их [веб-сайте](https://monerosupplies.com/2023/01/19/monerochan-irl/).

{{< youtube id="vFg5Bs4VRn4" autoplay="false" >}}  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![36](/img/post/2023-01-24-the-monero-moon-61/36.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![37](/img/post/2023-01-24-the-monero-moon-61/37.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования или недавно профинансированные:**_

В настоящий момент проекты, требующие финансирования, в системе CCS отсутствуют, но вы по-прежнему можете поддержать Проект Monero, пожертвовав в основной фонд Monero.

![38](/img/post/2023-01-24-the-monero-moon-61/38.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

Читайте этот исчерпывающий [твит](https://twitter.com/johnfoss69/status/1611240975506214913?s=20), опубликованный Джоном Фосом (да-да, мной), где рассматриваются различные показатели, свидетельствующие о том, что возможности Monero будут только нарастать в 2023 году.

![39](/img/post/2023-01-24-the-monero-moon-61/39.png)  

[Morpheus](https://twitter.com/CryptoMorpheus_) из [Moneroj.net](https://moneroj.net/) опубликовал пост под названием «[Monero входит в 2023 год как доминирующий приватный актив](https://moneroj.net/article/Monero-begins-2023-as-the-privacy-sovereign/)». В нём анализируются показатели Monero за 2022 год и приводятся некоторые мысли в отношении того, что может произойти в 2023. Полностью статью можно прочитать [здесь](https://moneroj.net/article/Monero-begins-2023-as-the-privacy-sovereign/).

![40](/img/post/2023-01-24-the-monero-moon-61/40.png)  

На недельном графике XMR/USD Monero находится в восходящем ценовом тренде начиная с июня 2022 года и демонстрирует более высокие минимум и максимум. Более высокий максимум плюс более высокий минимум являются индикатором ожидаемого и продолжающегося роста стоимости актива.

![41](/img/post/2023-01-24-the-monero-moon-61/41.png)  

На месячном графике XMR/USD Monero пытается вырваться из нисходящего тренда начиная с мая 2021 года.

![42](/img/post/2023-01-24-the-monero-moon-61/42.png)  

---

![43](/img/post/2023-01-24-the-monero-moon-61/43.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 222 417 XMR
- Общая рыночная капитализация Monero: 2 743 021 366 USD
- Позиция в рейтенге Coinmarketcap: 23
- Цена XMR/USD: 179 USD
- Цена XMR/BTC: 0.007770 BTC
- [Цена на LocalMonero.co](https://localmonero.co/statistics?language=en): 195 USD
- Средний размер комиссии за проведение транзакции: 0.000032 XMR (0.058 USD)
- Хешрейт: 2.662 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![50](/img/post/2023-01-24-the-monero-moon-61/50.png)  
*https://miningpoolstats.stream/monero*

### _Для развлечения_

![44](/img/post/2023-01-24-the-monero-moon-61/44.png)  
*https://www.reddit.com/r/Monero/comments/10hkzvi/comment_if_you_are_going_to_monerotopia_2023_cant/*

![45](/img/post/2023-01-24-the-monero-moon-61/45.png)  
*https://twitter.com/MyMonero/status/1614344221892268034/photo/1*

{{< youtube id="PuZ9-Yj0C0Q" autoplay="false" >}}  

![46](/img/post/2023-01-24-the-monero-moon-61/46.png)  
*https://www.reddit.com/r/moonero/comments/10hcovz/word_on_the_street/https://twitter.com/monero_max/status/1611710219326787584/photo/1*

![47](/img/post/2023-01-24-the-monero-moon-61/47.png)  
*https://www.reddit.com/r/moonero/comments/10gbcnx/cbdc_vs_monero/*

![48](/img/post/2023-01-24-the-monero-moon-61/48.png)  
*https://twitter.com/monero_max/status/1611710219326787584/photo/1*

![49](/img/post/2023-01-24-the-monero-moon-61/49.png)  
*https://www.reddit.com/r/moonero/comments/10ejlsc/all_roads_lead_to_monero/*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`49koJtBLRCjcfqVD93fosJGKLYFPZuBUz1iRvqJdMz9yBXV93UgKdSyDSbwUkdsytdSRvwKZhRTPp3de4fXzcioQGAFzWUU`

---

_Источник: [The Monero Moon (Issue 61)](https://www.themoneromoon.com/p/the-monero-moon-issue-61)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
