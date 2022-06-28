---
title: "The Monero Moon (выпуск 47)"
date: "2022-06-24"
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

_Примечание: В этом выпуске The Monero Moon я попытался осветить все важные новости за последние две недели. Весьма вероятно, что некоторая информация была упущена из-за того, что я принимал участие в MoneroKon 2022, и из-за связанных с этим событием путешествий. Если я пропустил какую-либо важную информацию, пожалуйста, свяжитесь со мной, и я обязательно включу её. Вы также можете ознакомиться с Monero Observer. Это зарядит вас здоровой дозой новостного контента, связанного с Monero._

### _Разработка, новые версии и технологии_

Количество ежедневных транзакций Monero достигло рекордного уровня и 15 июня составило 42 244 транзакции!

![01](/img/post/2022-06-24-the-monero-moon-47/01.png)  
*https://moneroj.net/translog/*

[noot](https://github.com/noot) (также известная как Elizabethereum), разработчик метода [атомных свопов Monero-Ethereum](https://github.com/noot/atomic-swap), недавно поделилась новостями, проинформировав сообщество Monero о том, что пользовательский интерфейс теперь интегрирован с Metamask, и пользователи смогут подписывать и отправлять транзакции непосредственно посредством своего браузера. Всю необходимую информацию можно найти [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/277#note_16905).

![02](/img/post/2022-06-24-the-monero-moon-47/02.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/277#note_16905*

[benevanoff](https://www.reddit.com/user/benevanoff/) представил демоверсию Simpla Vendejo, приложения, которое для проверки платежей и отслеживания их в базе данных MySQL использует кошелёк Monero, предназначенный исключительно для просмотра. Это довольно простой способ самостоятельно развернуть свой интернет-магазин Monero. Вся дополнительная информация содержится в [этом посте](https://github.com/kayabaNerve/monero-secret-sharing).

![03](/img/post/2022-06-24-the-monero-moon-47/03.png)  
*https://www.reddit.com/r/Monero/comments/vgq1xn/demo_simpla_vendejo_a_simple_way_to_self_host_a/*

[kayabaNerve](https://github.com/kayabaNerve) поделился Monero Secret Sharing, инструментом для создания кошелька Monero, распределённого в соответствии с определённым количеством долей, необходимым для восстановления кошелька в целом. Обратите внимание, что это доказательство концепции, в рамках которой поддерживается создание адресов только в тестовой сети, а схема multisig пока не поддерживается. Всю необходимую информацию можно найти [здесь](https://github.com/kayabaNerve/monero-secret-sharing).

Вышла новая версия XMRig v6.18.0. В ней была реализована поддержка обновления сети Monero до версии v15. Всю необходимую информацию можно найти [здесь](https://github.com/xmrig/xmrig/releases/tag/v6.18.0).

![04](/img/post/2022-06-24-the-monero-moon-47/04.png)  
*https://github.com/xmrig/xmrig/releases/tag/v6.18.0*

Команда Penumbra, форка децентрализованной биржи Haveno, строго придерживающаяся принципов децентрализации и приватности, недавно опубликовала новый документ, описывающий техническое решение протокола. С документом можно ознакомиться по [этой ссылке](https://gitlab.com/l0nelyc0w/penumbra/-/issues/21/).

![05](/img/post/2022-06-24-the-monero-moon-47/05.png)  
*https://gitlab.com/l0nelyc0w/penumbra/-/issues/21/*

Также Haveno предлагает вознаграждение в размере 2 XMR за восстановление вкладки Funds (Средства) в унаследованном десктоп-приложении Bisq. Всю дополнительную информацию можно получить, ознакомившись с [этим постом](https://github.com/haveno-dex/haveno/issues/319).

![06](/img/post/2022-06-24-the-monero-moon-47/06.png)  
*https://github.com/haveno-dex/haveno/issues/319*

MasFlam открыл доступ к исходному коду своего бота MoneroChad для Discord. MoneroChad — это бот Discord, который в основном выдаёт команды, связанные с Monero и криптовалютой. Найти его можно [здесь](https://github.com/MasFlam/MoneroChad).

mj опубликовал свой отчёт по разработке за период с мая по июнь 2022 г. В отчёте приводятся подробности работы mj над алгоритмом выбора ложных выходов и SolOptXMR. Полный текст отчёта можно найти [здесь](https://www.reddit.com/r/Monero/comments/vf7bcn/mjs_dev_report_mayjune_2022_33/).

xmrvsbeast опубликовал объявление, предназначенное для операторов публичных узлов, реализовавших поддержку zmq для P2Pool. Согласно объявлению, порт, используемый по умолчанию для zmq P2Pool, конфликтует с портом monerod Tor, и поэтому узлы должны быть настроены на соединение через порт 18084. Вся дополнительная информация содержится в [этом посте](https://www.reddit.com/r/Monero/comments/vga773/psa_to_public_node_operators_that_have_enabled/).

[Monero Observer](https://www.monero.observer/) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-24-2022/).

![07](/img/post/2022-06-24-the-monero-moon-47/07.png)  
*https://monero.observer/monero-dev-activity-report-week-24-2022/*

Если вы ещё не в курсе, 16 июля 2022 года на высоте блока 2 668 888 Monero планирует произвести обновление сети (хардфорк). Это будет согласованное сообществом Monero обновление сети, призванное повысить уровень приватности и общей производительности. Всем пользователям необходимо обновить программное обеспечение. Новая версия v0.18 Fluorine Fermi будет опубликована за месяц до сетевого обновления, то есть примерно 16 июня. В рамках обновления будет реализован целый ряд новых функций, среди прочего:
- размер кольца будет увеличен с 11 до 16 в целях повышения приватности;
- будут реализованы теги просмотра, в результате чего время синхронизации сократится на 40%;
- после введения Bulletproofs+ размер транзакций уменьшится примерно на 7%, равно как и время верификации, которое также сократится на 7%.

Также вместе с новым программным обеспечением вскоре будет опубликован полный список улучшений и усовершенствований. Если вы хотите узнать больше о грядущем обновлении сети Monero, пожалуйста, ознакомьтесь с [этим постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html) на официальном [веб-сайте Monero](https://www.getmonero.org/).

![08](/img/post/2022-06-24-the-monero-moon-47/08.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*

Если вы желаете помочь с обновлением сети Monero, достаточно просто уведомить о нём провайдеров кошельков и биржевых сервисов. Пожалуйста, сверьтесь с этим [контрольным листом](https://github.com/monero-project/meta/issues/690), чтобы все надлежащим образом обновили своё программное обеспечение и внесли соответствующие изменения.

![09](/img/post/2022-06-24-the-monero-moon-47/09.png)  
*https://github.com/monero-project/meta/issues/690*

Кроме того, вы можете помочь в тестировании и выявить ошибки в основной версии протокола Monero. Сделать это можно в тестовой сети. Соответствующие тестовые средства (tXMR) доступны абсолютно любому желающему! Дополнительную информацию, связанную с возможным оказанием помощи, можно найти в [этом посте](https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/), опубликованном garth_xmr.

![10](/img/post/2022-06-24-the-monero-moon-47/10.png)  
*https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/*

Seth For Privacy также просит помочь в тестировании кода Monero. Он попытался сделать процесс как можно проще, опубликовав новый образ Docker, и теперь любой пользователь Ubuntu сможет просто воспользоваться ссылкой, приведённой выше, и начать тестирование. Если вы используете другую операционную систему, такую как Windows, [свяжитесь с Seth](https://www.reddit.com/r/Monero/comments/utzyyz/help_test_out_the_upcoming_monero_network_upgrade/), и он сделает всё возможное, чтобы помочь вам.

![11](/img/post/2022-06-24-the-monero-moon-47/11.png)  
*https://paste.sethforprivacy.com/?96466ca9ad3f3d90#4fTCXio2b3S6fX5b2YHffzY6zpYsj3bJrgZh7Gmi8ESC*

### _Прочие новости_

Рабочая группа сообщества Monero приступала к публикации видео с Monero Konferenco 2022, конференции, посвящённой Monero, которая состоялась в Лиссабоне в прошлые выходные. Первые два видео можно посмотреть здесь или ниже.

{{< youtube id="r_vH-NyOYAg" autoplay="false" >}}  

{{< youtube id="g_ehNdMsPIM" autoplay="false" >}}  

Говард Чу, также выступивший на MoneroKon 2022, [выложил в общий доступ](http://highlandsun.com/hyc/20220618-Monerokon.pdf) свои слайды, которые использовались во время его выступления, посвящённого децентрализации майнинга Monero (Decentralizing Monero Mining).

![12](/img/post/2022-06-24-the-monero-moon-47/12.png)  

Monero Talk также опубликовали специальный выпуск с интервью с участниками недавней конференции MoneroKon 2022, прошедшей в Лиссабоне в прошлые выходные! Посмотрите выпуск можно здесь или ниже.

{{< youtube id="6VMcLzGYJV8" autoplay="false" >}}  

Несколько дней назад на Monero.com, странице в Twitter, было проведено мероприятие Twitter Space. Подробности здесь!

![13](/img/post/2022-06-24-the-monero-moon-47/13.png)  

Вышел шестнадцатый выпуск The Monero Standard. Ознакомиться с ним можно [здесь](https://localmonero.co/the-monero-standard/weekly/16), на веб-сайте LocalMonero.co!

Также был опубликован выпуск Revuo Monero №125. Соответствующие новости Monero можно найти [здесь](https://revuo-xmr.com/issue-125.html).

Bitcoin снова попал под пристальное внимание разработчиков криптовалют — Питер Тодд указал на потенциальные проблемы с долгосрочной безопасностью блокчейна, опирающейся только на транзакции для стимулирования майнеров.

![14](/img/post/2022-06-24-the-monero-moon-47/14.png)  

Как сообщается, США стремятся использовать монетарную политику для «положительной» дискриминации по расовому признаку до тех пор, пока в результате не будет достигнуто определённое равенство.

![15](/img/post/2022-06-24-the-monero-moon-47/15.png)  

Пользователь Reddit сообщил, что Китай хочет потребовать проверки личности интернет-пользователей для их допуска к участию в онлайн-обсуждениях. Ознакомьтесь с этим постом, содержащем всю дополнительную информацию.

![16](/img/post/2022-06-24-the-monero-moon-47/16.png)  
*https://www.reddit.com/r/China/comments/vgrwz1/new_more_severe_antiinternet_free_speech_rules_by/*

### _Мероприятия_

Судя по всем отзывам, конференция MoneroKon 2022 прошла с большим успехом и, благодаря Covid, стала первым подобным мероприятием с 2019 года. В конференции приняли участие самые разные докладчики, и все отлично провели время. Следите за [Monero Konferenco в Twitter](https://twitter.com/MoneroKon/) и оставайтесь в курсе всех новостей, связанных с этим событием.

![17](/img/post/2022-06-24-the-monero-moon-47/17.jpeg)  

![17](/img/post/2022-06-24-the-monero-moon-47/17.png)  

Встреча Исследовательской лаборатории Monero состоится в среду, 29 июня. Планируется обсуждение таких вопросов, как алгоритмы выбора ложных выходов и анализ аномального объёма транзакций. Соответствующие ссылки и дополнительную информацию о встрече можно найти [здесь](https://monero.observer/monero-research-lab-meeting-1-june-2022/#fn:14) благодаря Monero Observer. Встреча лаборатории MRL начнётся в 17:00 UTC на IRC-канале #monero-research-lab. Заглядывайте, если вам интересно, и увидите всё сами в режиме реального времени.

### _Биржи и предприниматели_

Cake Labs объявили, о скором открытии торговой площадки, где будут продаваться подарочные карты, которые можно будет приобрести со скидкой за XMR с помощью кошельков Cake Wallet и Monero.com. Эта услуга будет доступна только пользователям из США. Также ими был реализован автоматический маршрутизатор обмена, чтобы перед обменом других валют на XMR и обратно пользователи могли узнать котировки. Более подробная информация содержится в этом видео, опубликованном на YouTube!

{{< youtube id="4k9yWVURNkY" autoplay="false" >}}  

Также открылась торговая площадка Ghostnet. Ghostnet — это стихийная P2P торговая площадка, на которой используется исключительно криптовалюта и где можно найти списки рабочих вакансий, товаров и услуг, среди которых предлагаются в том числе консалтинговые и другие приватные услуги. На этой площадке можно торговать, как на Amazon, или бесплатно публиковать собственные рекламные объявления. Подробности можно узнать [здесь](https://ghostnet.id/).

![18](/img/post/2022-06-24-the-monero-moon-47/18.png)  

Пользователь субреддита Monero продаёт 1 акр сельскохозяйственной земли в Индии за 500 XMR. Если вы проживаете в Индии и вас заинтересовало предложение, читайте [этот пост](https://www.reddit.com/r/Monero/comments/vghrfc/re_ill_sell_my_1_acre_farm_in_india_for_500_xmr/), в котором содержится более подробная информация.

![19](/img/post/2022-06-24-the-monero-moon-47/19.jpeg)  
*https://www.reddit.com/r/Monero/comments/vghrfc/re_ill_sell_my_1_acre_farm_in_india_for_500_xmr/*

OKX теперь поддерживает спотовые торговые пары XMR/USDC.

![20](/img/post/2022-06-24-the-monero-moon-47/20.png)  

Представители Poloniex, давно существующей и, некоторым образом, противоречивой биржи, поддерживающей торговые пары XMR, объявили о возобновлении работы своего кошелька Monero для вывода средств спустя два месяца отключения.

![21](/img/post/2022-06-24-the-monero-moon-47/21.png)  

WideVPN теперь принимают оплату в XMR и предлагают год бесплатной подписки, если вы платите с помощью Monero. Для получения дополнительной информации ознакомьтесь с [этим постом](https://www.reddit.com/r/Monero/comments/vh803m/widevpn_now_accept_monero/).

![22](/img/post/2022-06-24-the-monero-moon-47/22.png)  
*https://www.reddit.com/r/Monero/comments/vh803m/widevpn_now_accept_monero/*

Ирина, главный исполнительный директор агрегатора криптовалютных бирж Swapzone.io, недавно провела дискуссию «Спроси меня о чём угодно» на субреддите Monero. Подробности можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ve7424/hi_all_irina_the_coo_of_crypto_exchange/).

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![23](/img/post/2022-06-24-the-monero-moon-47/23.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![24](/img/post/2022-06-24-the-monero-moon-47/24.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![25](/img/post/2022-06-24-the-monero-moon-47/25.png)  
*https://ccs.getmonero.org/funding-required/*

Веб-сайт Monero Bounties, альтернативу традиционной системе CCS Monero, можно использовать для сбора средств с целью решения задач, связанных с Monero. [john_r365 запрашивает финансирование](https://bounties.monero.social/posts/69/add-bounty-funded-amount-to-the-home-index-bounty-header), чтобы добавить собираемую сумму на домашнюю страницу и к заголовку веб-сайта Monero Bounties. Пример показан ниже.

![26](/img/post/2022-06-24-the-monero-moon-47/26.jpeg)  
*https://bounties.monero.social/posts/69/add-bounty-funded-amount-to-the-home-index-bounty-header*

Со слов ведущего разработчика Оскара Мире, проект Molly.im, являющийся форком Signal и направленный на интеграцию Monero, не уложится в предложенные сроки. Одна из причин связана с падением цен на XMR, случившимся после получения финансирования посредством CCS.

![27](/img/post/2022-06-24-the-monero-moon-47/27.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/252#note_16871*

### _Торговля и биржевые спекуляции_

[FlokiCrypto](https://www.tradingview.com/chart/XMRUSD/UPqvbttu-XMR-Diagonal-for-Macro-wave-1-primed-for-its-5/) прогнозирует падение цены перед тем, как пара XMR/USD пойдёт вверх.

![28](/img/post/2022-06-24-the-monero-moon-47/28.png)  
*https://www.tradingview.com/chart/XMRUSD/UPqvbttu-XMR-Diagonal-for-Macro-wave-1-primed-for-its-5/*

Solldy настроен оптимистично и предрекает [начало бычьего тренда](https://www.tradingview.com/chart/XMRUSD/orAp66dk-XMRUSD-declining-volatility/), учитывая снижение волатильности и разворот цены после того, как пара XMR/USD попала в зону ликвидности.

![29](/img/post/2022-06-24-the-monero-moon-47/29.png)  
*https://www.tradingview.com/chart/XMRUSD/orAp66dk-XMRUSD-declining-volatility/*

_**Показатели**_
- Общее количество Monero в обращении: 18 138 691 XMR
- Общая рыночная капитализация Monero: 2 249 667 081 USD
- Позиция в рейтенге Coinmarketcap: 28
- Цена XMR/USD: ~124 USD
- Цена XMR/BTC: 0.00588 BTC
- Цена на LocalMonero.co: 146 USD
- Средний размер комиссии за проведение транзакции: 0.000068 XMR ($0.0084)
- Хешрейт: 2.5553 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![30](/img/post/2022-06-24-the-monero-moon-47/30.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![31](/img/post/2022-06-24-the-monero-moon-47/31.jpeg)  
*https://www.reddit.com/r/Monero/comments/vi3bh3/love_seeing_these_wish_it_was_all_mine_lol/*

![32](/img/post/2022-06-24-the-monero-moon-47/32.jpeg)  
*https://www.reddit.com/r/moonero/comments/vbaach/never_let_them_see_you_bleed/*

![33](/img/post/2022-06-24-the-monero-moon-47/33.png)  
*https://www.reddit.com/r/Monero/comments/vi47b2/art_monero_is_private_and_free_money/*

![34](/img/post/2022-06-24-the-monero-moon-47/34.jpeg)  
*https://twitter.com/afungibleX/status/1538307815139328006/photo/1*

![35](/img/post/2022-06-24-the-monero-moon-47/35.jpeg)  
*https://www.reddit.com/r/moonero/comments/vf3ius/untraceable/*

![36](/img/post/2022-06-24-the-monero-moon-47/36.jpeg)  
*https://twitter.com/DontTraceMeBruh/status/1537880443982258178?s=20&t=dQ1ZEQpjkA_3rGxufom5rg*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 47)](https://www.themoneromoon.com/p/the-monero-moon-issue-47?sd=pf)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
