---
title: "The Monero Moon (выпуск 53)"
date: "2022-08-04"
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

Запланированное обновление сети Monero (хардфорк) состоится 13 августа 2022 г. на высоте блока 2 688 888. Программное обеспечение, которое будет необходимо установить в целях обеспечения соответствия обновлению сети, уже вышло (v0.18 Flourine Fermi), и его можно скачать на официальном веб-сайте Monero [www.getmonero.org](https://www.getmonero.org/downloads/). У всех пользователей есть пара недель для перехода. Если вы пользуетесь мобильным кошельком или каким-либо сторонним приложением, убедитесь в том, что у вас установлена актуальная версия. Если у вас возникнут вопросы, пожалуйста, свяжитесь с членами сообщества Monero на канале [r/Monero](http://www.reddit.com/r/monero) или с помощью другой социальной платформы.

![01](/img/post/2022-08-04-the-monero-moon-53/01.png)  

В рамках обновления будет реализован целый ряд новых функций, среди прочего:
- размер кольца будет увеличен с 11 до 16 в целях повышения приватности;
- будут реализованы теги просмотра, в результате чего время синхронизации сократится на 40%;
- после введения Bulletproofs+ размер транзакций уменьшится примерно на 7%, равно как и время верификации, которое также сократится на 7%.

Также вместе с новым программным обеспечением вскоре будет опубликован полный список улучшений и усовершенствований. Если вы хотите узнать больше о грядущем обновлении сети Monero, пожалуйста, ознакомьтесь с [этим постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html) на официальном [веб-сайте Monero](https://www.getmonero.org).

![02](/img/post/2022-08-04-the-monero-moon-53/02.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*  

Если вы желаете помочь с обновлением сети Monero, достаточно просто уведомить о нём провайдеров кошельков и биржевых сервисов. Пожалуйста, сверьтесь с этим [контрольным листом](https://github.com/monero-project/meta/issues/690), чтобы все надлежащим образом обновили своё программное обеспечение и внесли соответствующие изменения.

![03](/img/post/2022-08-04-the-monero-moon-53/03.png)  
*https://github.com/monero-project/meta/issues/690*  

Всё ещё интересно, что такое обновление сети (хардфорк) и что это означает для Monero? Читайте тред из Twitter, приведённый ниже, в котором кратко рассказывается о хардфорке и истории обновлений сети Monero.

![04](/img/post/2022-08-04-the-monero-moon-53/04.png)  

[RINOwallet](https://test.rino.io/), новый некастодиальный кошелёк Monero корпоративного уровня с поддержкой мультиподписей, содержит множество различных ресурсов и руководств, которые помогут вам подготовиться к обновлению сети Monero, которое состоится в августе. Переходите по [этой ссылке](https://www.reddit.com/r/Monero/comments/w4he13/resources_for_the_upcoming_hardfork/)! Там же вы найдёте крутые часы обратного отсчёта!

Следует отметить, что часы обратного отсчёта до хардфорка от RINOwallet сломались! Пользуйтесь оригинальными часами XMR, которые можно найти по ссылке: [xmr.noctism.com](https://xmr.noctism.com/)! До хардфорка осталось всего 9 дней!

![05](/img/post/2022-08-04-the-monero-moon-53/05.png)  
*https://xmr.noctism.com/*  

[MineXMR](https://minexmr.com/), самый большой майнинг-пул Monero, закроется 12 августа (непосредственно перед обновлением сети), и пользователям рекомендуется перейти на [P2Pool](https://p2pool.io/#pool). Если вы занимаетесь майнингом Monero с помощью MineXMR, вам необходимо реконфигурировать свои майнеры до 12 августа. Рекомендуется переключиться на P2Pool, децентрализованный майнинг-пул Monero. Это обеспечит постоянную защиту сети. Убедитесь в том, что у вас установлены версии Monerod [v0.18.0.0](https://www.getmonero.org/downloads/#cli) и P2Pool [v2.2.1](https://github.com/SChernykh/p2pool/releases/latest), чтобы быть готовыми к обновлению, которое состоится 13 августа.

![06](/img/post/2022-08-04-the-monero-moon-53/06.png)  
*https://minexmr.com/*  

Хешрейт MineXMR начинает падать, о чём свидетельствует график, приведённый ниже. В течение последних нескольких месяцев MineXMR принадлежало примерно 38-40% всего хешрейта, и в какой-то момент им даже пришлось повысить размер комиссий, чтобы майнеры перешли в другие пулы. Если вам интересно, что будет со всеми майнерами, которые занимаются майнингом в MineXMR, ознакомьтесь с [этими размышлениями](https://twitter.com/DontTraceMeBruh/status/1553052999831928832?s=20&t=Dv-2rh-fghgzCDicBAPxHQ).

![07](/img/post/2022-08-04-the-monero-moon-53/07.png)  
*https://minexmr.com/pools.html*  

Следуйте примеру JubJubByrd, уже обновившему свой [PiNode](https://pinode.co.uk/) и готовому к обновлению сети. Если вы хотите создать узел Monero с помощью Raspberry Pi, следуйте инструкциям из этого видео от [Motherland Engineering](https://www.youtube.com/channel/UCy-UNVS95Mkoqt8pQjwe9_g). Также вы можете воспользоваться этим [замечательным и простым руководством](https://www.reddit.com/r/Monero/comments/wdkszr/have_an_old_unused_laptop_create_your_own/), опубликованным [shermand100](https://www.reddit.com/user/shermand100/).

![08](/img/post/2022-08-04-the-monero-moon-53/08.png)  

{{< youtube id="riK8t_4llXw" autoplay="false" >}}  

Члены сообщества Monero уже переключились на P2Pool и могут подтвердить наличие выплат (даже если они совсем небольшие)!

![09](/img/post/2022-08-04-the-monero-moon-53/09.png)  

[AsBenDoge](https://github.com/AsBenDoge/p2pool-report) написал скрипт, генерирующий отчёты о доходах, полученных в результате майнинга в P2Pool, в формате .pdf.

![10](/img/post/2022-08-04-the-monero-moon-53/10.png)  
*https://www.reddit.com/r/Monero/comments/wbz7a0/i_made_a_script_which_generates_a_report_of_your/*  

Monero Supplies [рассматривают возможность](https://www.reddit.com/r/Monero/comments/wbkd8d/checking_if_anyone_would_be_interested_in_a/) продажи полных plug & play узлов, предназначенных для тех, кто ищет дополнительного удобства при создании и поддержке узлов Monero. Уже существовал веб-сайт, продававший узлы Monero, но, насколько мне известно, он просуществовал недолго, так что, если вас заинтересовало это предложение, дайте знать [monerobull](https://www.reddit.com/r/Monero/comments/wbkd8d/checking_if_anyone_would_be_interested_in_a/).

![11](/img/post/2022-08-04-the-monero-moon-53/11.png)  
*"Компактный" узел Monero - https://www.reddit.com/r/Monero/comments/wbkd8d/checking_if_anyone_would_be_interested_in_a/*  

Вышла новая версия [Monero-Bash v1.7.0](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.7.0). Monero-bash — это оболочка/менеджер Linux для monerod, monero-wallet-cli, XMRig и P2Pool. Как показано на [этом видео](https://www.reddit.com/r/Monero/comments/u0s8z5/monerobash_v100_released/), вы можете использовать monero-bash для скачивания, настройки и майнинга в P2Pool, и всё это займёт буквально пару минут. И не забывайте, [monero-bash v2.0.0](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.7.0) уже в разработке, так что скоро версии v1.x.x станут несовместимыми.

![12](/img/post/2022-08-04-the-monero-moon-53/12.png)  
*https://github.com/hinto-janaiyo/monero-bash/*  

Selsta опубликовал ежемесячный июльский отчёт по своей работе в рамках предложения, размещённого в CCS. Среди прочих вещей selsta занимался интеграцией Monero в аппаратный кошелёк Ledger с целью подготовки к хардфорку, а также исправил некоторые ошибки в GUI-кошельке. С отчётом можно ознакомиться по [этой ссылке](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/312#note_18095).

![13](/img/post/2022-08-04-the-monero-moon-53/13.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/312#note_18095*  

Любимый «дедушка» Monero, Crypto Grampy, поделился обновлением браузерной торговой точки Monero HotShop. Если вы, будучи онлайн-предпринимателем, хотите принимать оплату в XMR, читайте твит ниже!

![14](/img/post/2022-08-04-the-monero-moon-53/14.png)  

Хотите узнать, как развивается разработка децентрализованных бирж, ориентированных на Monero? Тогда читайте [этот пост](https://www.reddit.com/r/Monero/comments/we14wp/this_week_in_monero_decentralized_exchanges/), опубликованный [OsrsNeedsF2P](https://www.reddit.com/user/OsrsNeedsF2P/), в котором содержится исчерпывающий обзор текущих разработок.

![15](/img/post/2022-08-04-the-monero-moon-53/15.png)  
*https://monero.observer/monero-dev-activity-report-week-30-2022/*  

[Monero Observer](https://www.monero.observer/) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-30-2022/).

![16](/img/post/2022-08-04-the-monero-moon-53/16.png)  
*https://monero.observer/monero-dev-activity-report-week-30-2022/*  

Зафиксировано рекордное количество транзакций Monero, совершённых за один месяц. В июле 2022 года оно составило 963 209 транзакций. На приведённом ниже графике показан постепенный рост этого показателя начиная с 2019 года!

![17](/img/post/2022-08-04-the-monero-moon-53/17.png)  
*https://moneroj.net/transmonth/*  

Ежемесячный процент транзакций XMR относительно BTC продолжает расти. В июле он достиг 12,5%, и это уже второй месяц подряд!

![18](/img/post/2022-08-04-the-monero-moon-53/18.png)  
*https://moneroj.net/percentmonth/*  

### _Прочие новости_

Monero Talk взяли интервью у Люка Паркера (Luke Parker), также известного как kabayaNerve. Обсуждалась разработка интеграции SeraiDEX и Monero и множество других вопросов. Интервью можно найти по [этой ссылке](https://www.youtube.com/watch?v=5jGICOaeHzE).

{{< youtube id="5jGICOaeHzE" autoplay="false" >}}  

Alex из LocalMonero.co опубликовал на YouTube обсуждение/дебаты с [The Hated One](https://www.youtube.com/c/TheHatedOne), YouTube-каналом, насчитывающим более 350 000 подписчиков. Обсуждались Monero, Bitcoin, вопросы экономики и приватности. Видео можно найти [здесь](https://www.youtube.com/watch?v=H2I8cBpsUnc).

{{< youtube id="H2I8cBpsUnc" autoplay="false" >}}  

AlexAnarcho принял участие подкасте The Web3 Podcast, где обсуждался проект Monero. Послушать подкаст можно по [этой ссылке](https://d3ctxlq1ktw2nl.cloudfront.net/staging/2022-6-29/278554205-44100-2-364131257d15a.m4a) или в твите, размещённом ниже.

![19](/img/post/2022-08-04-the-monero-moon-53/19.png)  

Члены сообщества Monero схлестнулись с более широким сообществом Bitcoin в обсуждении Monero на [Stacker News](https://stacker.news/items/52018). Сторонники Monero столкнулись с некоторыми выдающимися «адвокатами» Bitcoin, в результате чего получилась [стоящая прочтения дискуссия](https://stacker.news/items/52018).

Monero Observer опубликовали двенадцатый выпуск Monero Observer Blitz за июль 2022. Ознакомившись с ним, вы узнаете всё, что происходило в сообществе Monero в июле. Найти новый выпуск можно [здесь](https://monero.observer/monero-observer-blitz-july-2022/).

На прошлой неделе вышел [двадцать первый выпуск](https://localmonero.co/the-monero-standard/weekly/21) The Monero Standard. Очередная доза свежих еженедельных новостей Monero уже ждёт вас!

Monero Talk также опубликовали новый великолепный эпизод [Monerotopia №76](https://www.youtube.com/watch?v=udXnsyYNF1c), в котором были охвачены все новости Monero, а также включён отчёт по цене XMR.

{{< youtube id="udXnsyYNF1c" autoplay="false" >}}  

Если вы ещё не видели, то обязательно должны посмотреть «Monero обязательно убьёт Bitcoin, и вот почему!» (Monero Is Out To KILL Bitcoin; Here’s Why!) от [Hone Crypto](https://www.youtube.com/c/HoneCrypto). Это прекрасный обзор Monero, даже несмотря на пару неточностей. Другое, более новое видео, в котором сравниваются приватные монеты, можно найти [здесь](https://www.youtube.com/watch?v=TOSg3_Jzzm4).

{{< youtube id="uMDtyKYCoPk" autoplay="false" >}}  

[WAM сообщает](https://www.wam.ae/en/details/1395303071688), что Израиль запретил использование наличных при совершении сделок на сумму более 4400 USD физическими лицами и более 1760 USD предпринимателями. Как было сказано на израильском канале i24 News, тем, кто нарушит закон, придётся уплатить штраф в размере 15 и 30 процентов от суммы соответствующей транзакции. Запрет был введён в рамках борьбы, которую страна ведёт с финансовыми преступлениями, которые совершаются с помощью цифровых платёжных платформ. [Cointelegraph](https://cointelegraph.com/news/israel-puts-the-brakes-on-cash-to-spur-digital-payments) также сообщает, что в будущем ожидаются и дальнейшие ограничения: будет запрещено хранение средств, превышающих 58 660 USD, 200 000 шекелей, в наличных в частных домовладениях.

![20](/img/post/2022-08-04-the-monero-moon-53/20.png)  

### _Встречи и мероприятия_

Встреча Исследовательской лаборатории Monero (MRL) будет проведена в среду, 3 августа, в 17:00 UTC. Соответствующие ссылки и дополнительную информацию о встрече, благодаря Monero Observer, можно найти [здесь](https://monero.observer/monero-research-lab-meeting-10-august-2022/). Встреча лаборатории MRL пройдёт на IRC-канале #monero-research-lab. Заглядывайте и увидите всё сами в режиме реального времени.

Теперь каждую субботу будут проводиться игры Monero Poker Nights, где вы сможете поиграть в техасский холдем со своими товарищами по проекту Monero. Игры будут проводиться через сеть Tor и, будем надеяться, с использованием XMR. И при этом никаких KYC! На этой неделе игра состоится в 22:00 UTC, а затем это будет происходить раньше, чтобы привлечь больше игроков из разных временных поясов. Всю дополнительную информацию можно найти в [этом посте](https://www.reddit.com/r/Monero/comments/wc35it/monero_poker_night/).

4 августа 2022 г. в 17:00 в Кейптауне, Южная Африка, в ресторане La Parada также пройдёт встреча сообщества Monero. Более подробную информацию можно найти [здесь](https://www.meetup.com/cape-town-privacy-meetup-group/events/287148562/). Ходят слухи, что там [будет присутствовать член Monero Core Team Fluffypony](https://twitter.com/MyMonero/status/1552217228132712448?s=20&t=mrZC-AFR9rrdR6Q8kYuIIQ). Так что приезжайте, если хотите поприветствовать его лично!

![21](/img/post/2022-08-04-the-monero-moon-53/21.png)  
*https://www.meetup.com/cape-town-privacy-meetup-group/events/287148562/*  

9 августа в Нью-Йорке по адресу 447 Broadway, 2nd Floor в 16:30 [Cake Wallet](https://twitter.com/cakewallet) и [Monerotopia](https://www.youtube.com/c/MoneroTalk) проведут встречу сообщества Monero. [Kayaba](https://twitter.com/kayabanerve), также известный как Люк Паркер, выступит с презентацией, посвящённой децентрализованной бирже Serai, ориентированной на Monero. Кроме того, будет проводиться лотерея! Не забудьте оформить приглашение! Более подробную информацию можно найти здесь.

![22](/img/post/2022-08-04-the-monero-moon-53/22.png)  

### _Биржи и предприниматели_

Запущен новый веб-сайт [Monero Market](http://moneromarket.io/). Он похож на Ebay, использует систему условного депонирования и поддерживает XMR как единственное средство оплаты. Там уже доступны некоторые товары, так что заходите, чтобы купить или продать что-то за XMR!

![23](/img/post/2022-08-04-the-monero-moon-53/23.png)  
*https://moneromarket.io/*  

[Piconeroj.eu](https://piconeroj.eu/) — это новая торговая P2P площадка Monero, которая, [как утверждает monerobull](https://www.reddit.com/r/Monero/comments/wc7zx6/introducing_piconerojeu_an_xmrwow_only_p2p_market/), «является прекрасным имиджбордом, где треды заменены рекламными объявлениями в духе Крейглиста». Это очень похоже на тред 4chan. Сайт не использует cookies или JS, и доступ к нему можно получить через VPN или TOR. В настоящее время это альфа-версия, и им требуется протестировать, как люди смогут размещать свои объявления купли/продажи. Более подробная информация содержится в этом посте.

[AllArk](http://ttps/allark.io/), веб-сайт, позволяющий покупать предоплаченные карты Visa и подарочные карты через BTCpayserver, теперь принимает Monero. Следует отметить, что сервис работает только в США. Всю дополнительную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/wf1su4/allark_now_accepts_monero_for_prepaid_visa_and/) или в комментариях.

![24](/img/post/2022-08-04-the-monero-moon-53/24.png)  
*https://allark.io/*  

Как сообщалось на прошлой неделе, теперь вы можете купить XMR напрямую через кошелёк MyMonero с помощью фиатных сервисов. Более подробная информация содержится в твите ниже.

![25](/img/post/2022-08-04-the-monero-moon-53/25.png)  

[xInvestor](https://www.xinvestor.com/en_US/), относительно новая криптовалютная биржа, объявила, что теперь поддерживает XMR. Несмотря на то, что теперь на ней стала возможна торговля XMR, перед тем как пользоваться сервисом, следует проверить, допускает ли он вывод XMR.

![26](/img/post/2022-08-04-the-monero-moon-53/26.png)  

SessionID опубликовал на Incognito Chain твит на тему пулов ликвидности XMR. Оказывается, выплаты происходят только в криптовалюте локального блокчейна. С учётом непрерывной череды взломов DeFi следует помнить о всех необходимых мерах предосторожности, если вы считаете XMR ликвидным активом!

![27](/img/post/2022-08-04-the-monero-moon-53/27.png)  

Если вы обсуждаете Monero в соцсетях, имейте в виду: имелись случаи, когда мошенники писали пользователям личные сообщения и представлялись «службой поддержки» Monero. Такой службы не существует! Это децентрализованный проект. Никогда и никому не давайте своей мнемонической фразы или каких-либо личных данных. Если кто-то просит вас прислать свою мнемоническую фразу, то это на 99,99999% мошенник.

![28](/img/post/2022-08-04-the-monero-moon-53/28.png)  
*Monero scammer - https://www.reddit.com/r/Monero/comments/wce007/didnt_know_monero_had_a_24x7_customer_support/*

![29](/img/post/2022-08-04-the-monero-moon-53/29.png)  

### _Краудфандинговая система сообщества (CCS)_

В системе CCS размещено предложение о финансировании следующих 18 выпусков дайджеста The Monero Moon. Будет великолепно, если вы оставите свой комментарий [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/336).

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![30](/img/post/2022-08-04-the-monero-moon-53/30.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![31](/img/post/2022-08-04-the-monero-moon-53/31.png)  
*https://ccs.getmonero.org/ideas/*  

_**Проекты CCS, требующие финансирования:**_

![32](/img/post/2022-08-04-the-monero-moon-53/32.png)  
*https://ccs.getmonero.org/funding-required/*  

### _Торговля и биржевые спекуляции_

Ежемесячный график XMR/BTC. Monero по-прежнему усиливается относительно Bitcoin после успешного повторного прорыва в июне/июле 2022.

![33](/img/post/2022-08-04-the-monero-moon-53/33.png)  

![34](/img/post/2022-08-04-the-monero-moon-53/34.png)  

Ознакомьтесь с этим «бычьим» графиком, опубликованным ltc-joe под названием «[LARP Capital: Monero, USD и боевое крещение](https://www.tradingview.com/chart/XMRUSD/tJuDDcvd-LARP-Capital-Monero-USD-and-The-Baptism-of-Fire/)» (LARP Capital: Monero USD and The Baptism of Fire). Автор надеется на «новый исторический максимум в течение последующих 3-7 месяцев».

![35](/img/post/2022-08-04-the-monero-moon-53/35.png)  
*https://www.tradingview.com/chart/XMRUSD/tJuDDcvd-LARP-Capital-Monero-USD-and-The-Baptism-of-Fire/*

_**Показатели**_
- Общее количество Monero в обращении: 18 156 481 XMR
- Общая рыночная капитализация Monero: 2 935 294 148 USD
- Позиция в рейтенге Coinmarketcap: 28 (27 на прошлой неделе)
- Цена XMR/USD: 161 USD
- Цена XMR/BTC: 0,007091 BTC
- [Цена на LocalMonero.co](https://localmonero.co/statistics?language=en): 164 USD
- Средний размер комиссии за проведение транзакции: 0.000013 XMR (0.021 USD)
- Хешрейт: 2.420 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![36](/img/post/2022-08-04-the-monero-moon-53/36.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![37](/img/post/2022-08-04-the-monero-moon-53/37.png)  
*https://www.reddit.com/r/Monero/comments/wer159/xmr_poster_collection_by_sidarta0_2022/*

![38](/img/post/2022-08-04-the-monero-moon-53/38.png)  

![39](/img/post/2022-08-04-the-monero-moon-53/39.png)  
*https://monero.graphics/*

![40](/img/post/2022-08-04-the-monero-moon-53/40.png)  
*https://boards.4channel.org/biz/thread/50663419*

![41](/img/post/2022-08-04-the-monero-moon-53/41.png)  
*https://www.reddit.com/r/moonero/comments/wczh7g/the_moneromobile/*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 53)](https://www.themoneromoon.com/p/the-monero-moon-issue-53)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
