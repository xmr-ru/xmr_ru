---
title: "The Monero Moon (выпуск 55)"
date: "2022-08-17"
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

13 августа 2022 года на высоте блока 2 688 888 состоялось обновление сети Monero (хардфорк). 720 блоков спустя, на высоте 2 689 608, была активирована версия v16.

В рамках обновления был реализован целый ряд новых функций:
- размер кольца был увеличен с 11 до 16 в целях повышения приватности;
- были реализованы теги просмотра с целью сокращения времени синхронизации на 40%;
- реализация Bulletproofs+ должна уменьшить размер транзакций примерно на 7%, равно как и время верификации, которое также теперь сократится на 7%.

![01](/img/post/2022-08-17-the-monero-moon-55/01.png)  

Как сообщается, обновление прошло гладко, однако у некоторых провайдеров [сторонних кошельков](https://twitter.com/MyMonero/status/1559828547983867905?s=20&t=584UEUoJCs-MXd3krR5Adg) и [бирж](https://www.reddit.com/r/Monero/comments/wpg07z/withdrawals_not_working_on_kraken/) возникли небольшие проблемы, которые по большей части были исправлены. Следует отметить, что всем пользователям следует обновить программное обеспечение своих кошельков или узлов Monero, чтобы обеспечить совместимость с новой версией сети.

Вышла новая версия официальных CLI и GUI кошельков Monero, v0.18.1.0 Fluorine Fermi. Больше информации и ссылки для скачивания можно найти [здесь](https://www.getmonero.org/2022/08/11/monero-GUI-0.18.1.0-released.html) и [здесь](https://www.reddit.com/r/Monero/comments/wmtrs8/cli_gui_v01810_fluorine_fermi_ledger_monero_app/).

![02](/img/post/2022-08-17-the-monero-moon-55/02.png)  
*https://www.getmonero.org/2022/08/11/monero-GUI-0.18.1.0-released.html*  

Команда [COMIT](https://comit.network/) опубликовала очередную версию [xmr-btc-swap v0.11](https://www.reddit.com/r/Monero/comments/wly8of/xmrbtcswap_011_released_hard_fork_ready/). После обновления сети удобство и простота совершения атомных свопов XMR-BTC повысились. Также был реализован целый ряд других усовершенствований, с которыми можно ознакомиться по [этой ссылке](https://github.com/comit-network/xmr-btc-swap/releases/tag/0.11.0), а вся дополнительная информация размещена [здесь](https://www.reddit.com/r/Monero/comments/wly8of/xmrbtcswap_011_released_hard_fork_ready/).

![03](/img/post/2022-08-17-the-monero-moon-55/03.png)  
*https://github.com/comit-network/xmr-btc-swap/releases/tag/0.11.0*  

Также сообщается о выходе новой версии [Monero-Bash v1.8.0](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.8.0). Был реализован ряд новых функций, таких как отображение статистики P2Pool. Monero-bash — это оболочка/менеджер Linux для monerod, monero-wallet-cli, XMRig и P2Pool. Как показано на [этом видео](https://www.reddit.com/r/Monero/comments/u0s8z5/monerobash_v100_released/), вы можете использовать monero-bash для скачивания, настройки и майнинга в P2Pool, и всё это займёт буквально пару минут. И не забывайте, [monero-bash v2.0.0 уже в разработке](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.7.0), так что скоро версии v1.x.x станут несовместимыми.

![04](/img/post/2022-08-17-the-monero-moon-55/04.png)  
*https://www.reddit.com/r/Monero/comments/wqp62v/monerobash_v180_released/*  

Вышла новая версия v3.0.2 Monerujo, Android-кошелька Monero с поддержкой аппаратного кошелька Ledger. Вся необходимая информация содержится в [этом посте](https://www.reddit.com/r/Monerujo/comments/wnpur9/update_monerujo_v302_fluorine_fermi_upgrading_to/)!

![05](/img/post/2022-08-17-the-monero-moon-55/05.png)  
*https://www.monerujo.io/*  

Опубликована версия [Feather Wallet v2.1.0](https://www.reddit.com/r/FeatherWallet/comments/wmly8h/feather_wallet_210_released/). Feather Wallet — это бесплатный кошелёк Monero в стиле Electrum с целым набором удобных функций. Более подробно о последнем обновлении написано [здесь](https://www.reddit.com/r/FeatherWallet/comments/wmly8h/feather_wallet_210_released/), а [ссылки на скачивание](https://featherwallet.org/download/) последней версии можно найти на официальном веб-сайте Feather Wallet.

![06](/img/post/2022-08-17-the-monero-moon-55/06.png)  
*https://featherwallet.org/*  

Приложение Ledger Monero App также было обновлено до версии v1.8.0. Установив её, пользователи аппаратного кошелька Ledger обеспечат совместимость приложения с новой версией сети. Если вы используете Ledger со своим кошельком Monero, обязательно обновите приложение на Ledger. Все подробности можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/wmtrs8/cli_gui_v01810_fluorine_fermi_ledger_monero_app/).

![07](/img/post/2022-08-17-the-monero-moon-55/07.png)  

Сообщается об обновлении аппаратно-реализованного программного обеспечения Trezor. Вероятно, пользователям будет проще обновить его с помощью [Trezor Suite](https://suite.trezor.io), но точно так же новую версию можно скачать [здесь](https://github.com/trezor/trezor-firmware/releases/tag/core%2Fv2.5.2). Если у вас возникнут какие-либо проблемы, свяжитесь с командой [Trezor](https://twitter.com/Trezor).

![08](/img/post/2022-08-17-the-monero-moon-55/08.png)  

12 августа количество транзакций вновь стало рекордным, составив 61 305 транзакций.

![09](/img/post/2022-08-17-the-monero-moon-55/09.png)  
*https://moneroj.net/translin/#*  

Процент транзакций Monero относительно транзакций Bitcoin также был рекордно высоким — 22,8%.

![10](/img/post/2022-08-17-the-monero-moon-55/10.png)  
*https://moneroj.net/percentage/*  

Кроме того, тогда же, 12 августа, пул транзакций достиг размера 10 Мб!

![11](/img/post/2022-08-17-the-monero-moon-55/11.png)  

В ознаменование обновления сети Monero CryptoMorpheus_ опубликовал на [Moneroj.net](https://moneroj.net) 8 новых графиков, связанных с P2Pool, прибыльностью майнинга, а также отклонениями от закона Меткалфа (BTC). С графиками можно ознакомиться [здесь](https://www.reddit.com/r/Monero/comments/wpr25k/new_charts_released_on_monerojnet/).

![12](/img/post/2022-08-17-the-monero-moon-55/12.png)  

Команда MineXMR проинформировала майнеров о том, что закрытие пула MineXMR переносится на 19 августа. MineXMR рекомендует пользователям перейти к использованию децентрализованного майнинг-пула [P2Pool](http://ttps/p2pool.io/#pool). Все подробности изложены [здесь](https://minexmr.com/).

![13](/img/post/2022-08-17-the-monero-moon-55/13.png)  
*https://minexmr.com/*  

MineXMR был самым большим майнинг-пулом Monero. Несмотря на то, что самыми большими пулами теперь становятся supportxmr и nanopool, Hashvault, пожалуй, продемонстрировал самый значительный процент сетевого хешрейта, который в начале июля составлял примерно 2%, а сегодня уже равен 10%. За тот же период объём хешрейта P2Pool вырос с 4% до 6%.

![14](/img/post/2022-08-17-the-monero-moon-55/14.png)  

[Mindos2055](https://www.reddit.com/r/Monero/comments/wo7afz/left_my_pc_on_without_realising_i_was_mining_and/) невероятно повезло. Не каждому удаётся вычислить блок путём соло-майнинга всего спустя 30 минут после запуска компьютера, который пользователь оставил включённым и даже не сразу понял, что произошло.

![15](/img/post/2022-08-17-the-monero-moon-55/15.png)  

Хотите заняться майнингом Monero? [aFungible](https://twitter.com/afungibleX) написал «не техническое» руководство, ознакомившись с которым, вы узнаете, сколько можно заработать за день путём майнинга Monero. Само руководство можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/wr2ll0/this_is_how_much_you_can_earn_per_day_with_mining/).

![16](/img/post/2022-08-17-the-monero-moon-55/16.png)  
*https://www.reddit.com/r/Monero/comments/wr2ll0/this_is_how_much_you_can_earn_per_day_with_mining/*  

[Monero Observer](https://www.monero.observer) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-32-2022/).

![17](/img/post/2022-08-17-the-monero-moon-55/17.png)  
*https://monero.observer/monero-dev-activity-report-week-32-2022/*  


### _Прочие новости_

На прошлых выходных в рамках празднования обновления сети Monero [gnuteardrops](https://www.reddit.com/user/gnuteardrops/) из [monero.graphics](https://monero.graphics) опубликовал крутую инфографику. Подобную инфографику, которую вы можете абсолютно свободно использовать и которой можете смело делиться, вы найдёте на этом [веб-сайте](https://monero.graphics/about).

![18](/img/post/2022-08-17-the-monero-moon-55/18.png)  
*https://monero.graphics/all/monero-v15/*  

Ранее на этой неделе Monero Talk опубликовали эпизод №78 Monerotopia. В нём содержится еженедельный отчёт по цене XMR, обсуждение санкций, наложенных на Tornado Cash, обновление сети с Seth For Privacy и многое другое. Видео можно найти по [этой ссылке](https://www.youtube.com/watch?v=Oy2zkzw9MYk).

{{< youtube id="Oy2zkzw9MYk" autoplay="false" >}}  

Monero Talk также взяли интервью у Бенджамина Шаффера (Benjamin Shaffer), юрисконсульта Goldback, первой в мире компании, занимающейся производством физических, взаимозаменяемых золотых денег. Полностью интервью можно посмотреть [здесь](https://www.youtube.com/watch?v=74Kent24PZM).

{{< youtube id="74Kent24PZM" autoplay="false" >}}  

Сообщается, что голландские власти арестовали предполагаемого разработчика миксера Ethereum, известного как Tornado Cash. Это произошло вскоре после того, как Управление по контролю за иностранными активами (OFAC) Министерства финансов США наложило на миксер санкции. Обвинение, выдвинутое OFAC, заключается в том, что начиная с 2019 года посредством сервиса Tornado Cash якобы было отмыто 7 миллиардов USD в криптовалюте. Пока неизвестно, был ли разработчик Tornado Cash арестован за написание кода Tornado Cash (это опенсорс проект) или же по каким-то другим не связанным с этим причинам. Более подробно о санкциях, наложенных на Tornado Cash, можно прочитать [здесь](https://decrypt.co/107314/dutch-police-arrest-alleged-tornado-cash-dev-more-arrests-not-ruled-out-financial-crimes-unit). Если вас заинтересовала эта история и вы хотите и дальше следить за развитием ситуации, страница фонда [DeFi Education](https://twitter.com/fund_defi) в Twitter может послужить хорошим источником информации. Многие представители криптосообщества пристально следят за этим случаем, так как он может стать прецедентом для преследования разработчиков криптовалюты в будущем.

![19](/img/post/2022-08-17-the-monero-moon-55/19.png)  

В ответ на санкции, введённые против Tornado Cash, Coin Center, ведущая некоммерческая организация, занимающаяся политическими проблемами, с которыми сталкивается криптовалютное сообщество, опубликовала статью под заголовком «Анализ: что может, а что не может попасть под санкции в случае с Tornado Cash» (Analysis: What is and what is not a sanctionable entity in the Tornado Cash case).

![20](/img/post/2022-08-17-the-monero-moon-55/20.png)  
*https://www.coincenter.org/analysis-what-is-and-what-is-not-a-sanctionable-entity-in-the-tornado-cash-case/*  

Джастин Эренхофер (Justin Ehrenhofer), вице-президент по операциям Cake Wallet, дал интервью [Coin Desk](https://www.coindesk.com/policy/2022/08/16/tornado-cash-us-ban-is-bad-precedent-but-monero-was-made-for-this-cake-wallet-exec/), в котором, рассуждая о значении санкций, наложенных на Tornado Cash, для Monero, сказал следующее:

> «Для этого и был создан проект Monero. Если вас беспокоит вероятность того, что правительство начнёт преследовать какой-то определённый тип протокола или группу лиц, занимающихся поддержкой децентрализованной сети, то буквально ради того, чтобы этого избежать, проект и сообщество Monero начиная с 2014 года тратили все свои ресурсы».

Эренхофер отметил, что властям тяжело придётся в случае с Monero из-за алгоритма майнинга посредством CPU. Они ничего не смогут сделать с производителями аппаратного обеспечения, которое используется для майнинга Monero, в отличие от производителей ASIC для майнинга Bitcoin. Также он упомянул, что, благодаря приватности транзакций, майнеры не могут цензурировать их, и несмотря на то, что отдельно взятый адрес и может попасть под санкции, поскольку личность отправителя и получателя остаются скрытыми, массовая слежка за блокчейном Monero просто невозможна. Полную версию видео можно посмотреть [здесь](https://www.coindesk.com/policy/2022/08/16/tornado-cash-us-ban-is-bad-precedent-but-monero-was-made-for-this-cake-wallet-exec/) или ниже.

![21](/img/post/2022-08-17-the-monero-moon-55/21.png)  
*https://www.coindesk.com/policy/2022/08/16/tornado-cash-us-ban-is-bad-precedent-but-monero-was-made-for-this-cake-wallet-exec/*  

![22](/img/post/2022-08-17-the-monero-moon-55/22.png)

BleepingComputer в статье под названием «После хардфорка Monero, излюбленная монета хакеров станет ещё более приватной» ([Monero hard fork makes hackers' favorite coin even more private](https://www.bleepingcomputer.com/news/security/monero-hard-fork-makes-hackers-favorite-coin-even-more-private/)) цитирует Стива Уолбрёля (Steve Walbroehl), соучредителя [Halborn](https://halborn.com), фирмы, занимающейся проблемами безопасности блокчейнов:

![23](/img/post/2022-08-17-the-monero-moon-55/23.png)  
*https://www.bleepingcomputer.com/news/security/monero-hard-fork-makes-hackers-favorite-coin-even-more-private/*  

Ведущие сайты, публикующие новости, связанные с криптовалютой, не обошли вниманием обновление сети Monero:
- Coin Desk: «Важное обновление приватного криптовалютного протокола Monero» ([Crypto Privacy Protocol Monero Is Getting a Major Upgrade](https://www.coindesk.com/tech/2022/08/12/privacy-protocol-monero-is-getting-a-major-upgrade/)).
- Decrypt: «После хардфорка механизмы обеспечения приватности Monero усилятся» ([Monero Rolls Out Enhanced Privacy Features With Hard Fork](https://decrypt.co/107441/monero-rolls-out-enhanced-privacy-features-with-hard-fork)).
- Daily Coin: «Хардфорк Monero состоялся: встречайте улучшенные функции обеспечения безопасности и приватности» ([Monero Hard Fork Goes Live, Introduces Improved Security And Privacy Features](https://dailycoin.com/monero-hard-fork-goes-live-introduces-improved-security-and-privacy-features/)).

![24](/img/post/2022-08-17-the-monero-moon-55/24.png)  
*https://www.coindesk.com/tech/2022/08/12/privacy-protocol-monero-is-getting-a-major-upgrade/*  

![25](/img/post/2022-08-17-the-monero-moon-55/25.png)  
*https://decrypt.co/107441/monero-rolls-out-enhanced-privacy-features-with-hard-fork*  

![26](/img/post/2022-08-17-the-monero-moon-55/26.png)  
*https://dailycoin.com/monero-hard-fork-goes-live-introduces-improved-security-and-privacy-features/*  

### _Встречи и мероприятия_

Встреча Исследовательской лаборатории Monero будет проведена в среду, 24 августа, в 17:00 UTC. Соответствующие ссылки и дополнительную информацию о встрече, благодаря Monero Observer, можно найти [здесь](https://monero.observer/monero-research-lab-meeting-24-august-2022/). Встреча лаборатории MRL состоится на IRC-канале #monero-research-lab. Заглядывайте, если вам интересно, и увидите всё сами в режиме реального времени.

### _Биржи и предприниматели_

Команда Cake Wallet сообщает, что после форка Monero количество уникальных скачиваний Cake Wallet выросло на 50%, а количество скачиваний их кошелька Monero.com для iOS взлетело на все 110% по сравнению с предыдущей неделей. Количество установок на устройства Android также возросло: в случае Cake Wallet на 40%, а в случае кошелька Monero.com на 10%.

![27](/img/post/2022-08-17-the-monero-moon-55/27.png)  

Команда Cake Labs обновила условия использования Cake Pay и проинформировала пользователей, что для продолжения пользования сервисом потребуется предоставление их «провайдеру» ID приложения и адреса электронной почты. Это как-то скажется на вас только в том случае, если вы пользуетесь сервисом для приобретения подарочных карт Cake Pay. Более подробную информацию, связанную с Cake Pay, можно найти [здесь](https://www.reddit.com/r/Monero/comments/wpa19u/update_on_cake_pays_providers_requirement_of/).

Опция оплаты в XMR на [ShopInBi](https://shopinbit.com) некоторое время была [недоступна](https://www.reddit.com/r/Monero/comments/wqz0ga/xmr_is_available_again_on_shopinbit/) из-за последнего обновления BTCPayserver. Однако, благодаря [Seth For Privacy](https://twitter.com/sethforprivacy), проблема была исправлена, и теперь сервис снова принимает XMR онлайн. Более подробно обо всём рассказывается в [этом посте](https://www.reddit.com/r/Monero/comments/wqz0ga/xmr_is_available_again_on_shopinbit/). В настоящее время [ShopInBit](https://shopinbit.com/) тестируют новую функцию приватной доставки под названием Pickup & Meetup, и если вы проживаете в Германии, то можете попробовать воспользоваться ею.

![28](/img/post/2022-08-17-the-monero-moon-55/28.png)  
*https://www.reddit.com/r/Monero/comments/wqz0ga/xmr_is_available_again_on_shopinbit/*  

Как сообщается, после обновления сети целый ряд бирж не даёт вывести XMR. Согласно информации, опубликованной [MoneroFox](https://www.reddit.com/user/MoneroFox/), следующие биржи не позволяют вносить и выводить XMR:
- Kraken
- NiceHashEx
- Bitfinex
- HitBTC
- Gate
- TradeOgre

Также сообщается, что после небольшого перерыва Binance вновь подключила возможность депонирования и вывода.

### _Краудфандинговая система сообщества (CCS)_

В системе CCS размещено предложение о финансировании следующих 18 выпусков дайджеста The Monero Moon. Будет великолепно, если вы оставите свой комментарий [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/336). Заранее спасибо!

Фонд MAGIC Monero собирает средства на финансирование работы noot по реализации атомных свопов ETH-XMR. Соответствующую страницу GoFundMe можно найти по [этой ссылке](https://www.gofundme.com/f/noot-ethxmr-atomic-swap-development-4-months).

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![29](/img/post/2022-08-17-the-monero-moon-55/29.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![30](/img/post/2022-08-17-the-monero-moon-55/30.png)  
*https://ccs.getmonero.org/ideas/*  

_**Проекты CCS, требующие финансирования:**_

![31](/img/post/2022-08-17-the-monero-moon-55/31.png)  
*https://ccs.getmonero.org/funding-required/*  

### _Торговля и биржевые спекуляции_

Доминирующий показатель рыночной капитализации XMR растёт уже более чем в течение последних шести месяцев. Рост начался ещё в январе 2022.

![32](/img/post/2022-08-17-the-monero-moon-55/32.png)  

Недельный график XMR/BTC демонстрирует сопротивление на отметке примерно 0,0066 BTC, которая достигалась дважды, но сейчас уже произошёл «откат» до уровня поддержки. Если это нечто большее, чем просто «медвежье ралли», то можно надеяться на восходящий тренд.

![33](/img/post/2022-08-17-the-monero-moon-55/33.png)  

Предлагаем ознакомиться с отчётом по цене, составленным [aFungible](https://twitter.com/afungibleX) и опубликованным в эпизоде №78 Monerotopia.

{{< youtube id="fh7k7Q2K2L0" autoplay="false" >}}  

Mownehro опубликовал твит, в котором наглядно демонстрируется серьёзный объём заявок на приобретение XMR.

![34](/img/post/2022-08-17-the-monero-moon-55/34.png)  

[bawdyanarchist](https://www.reddit.com/user/bawdyanarchist/) поделился [интересными мыслями](https://www.reddit.com/r/xmrtrader/comments/wr4dyz/frozen_withdraws_price_suppression_a_recap_of_the/) в отношении изменения цены Monero в течение последних нескольких недель.

![35](/img/post/2022-08-17-the-monero-moon-55/35.png)  
*https://www.reddit.com/r/xmrtrader/comments/wr4dyz/frozen_withdraws_price_suppression_a_recap_of_the/*  

_**Показатели**_
- Общее количество Monero в обращении: 18 162 476 XMR
- Общая рыночная капитализация Monero: 3 055 155 579 USD
- Позиция в рейтенге Coinmarketcap: 27 (29 на прошлой неделе)
- Цена XMR/USD: 168 USD
- Цена XMR/BTC: 0.007177 BTC
- [Цена на LocalMonero.co](https://localmonero.co/statistics?language=en): 176 USD
- Средний размер комиссии за проведение транзакции: 0.000013 XMR (0.02 USD)
- Хешрейт: 2.471 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![36](/img/post/2022-08-17-the-monero-moon-55/36.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![37](/img/post/2022-08-17-the-monero-moon-55/37.png)  
*https://twitter.com/DontTraceMeBruh*  

![38](/img/post/2022-08-17-the-monero-moon-55/38.png)  
*https://twitter.com/BitcoinQ_A/status/1558064306083725312/photo/1*  

![39](/img/post/2022-08-17-the-monero-moon-55/39.png)  

![40](/img/post/2022-08-17-the-monero-moon-55/40.png)  
*https://twitter.com/tallhatdoug/status/1558525916552331266/photo/1*  

![41](/img/post/2022-08-17-the-monero-moon-55/41.png)  
*https://twitter.com/tallhatdoug/status/1558525916552331266/photo/1*  

![42](/img/post/2022-08-17-the-monero-moon-55/42.png)  

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 55)](https://www.themoneromoon.com/p/the-monero-moon-issue-55)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
