---
title: "The Monero Moon (выпуск 45)"
date: "2022-06-02"
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

Постэмиссия Monero начнётся примерно через шесть дней, 8 июня. Несколько недель назад в официальном аккаунте Monero в Twitter было опубликовано сообщение, в котором было описано, зачем Monero постэмиссия, как она работает и что это значит для рядовых пользователей. С твитом можно ознакомиться ниже.

![01](/img/post/2022-06-02-the-monero-moon-45/01.png)  

Ниже размещено видео доктора Кима, в котором разъясняется, что такое постэмиссия Monero, чем отличается её график от графика эмиссии Bitcoin, а также почему это правильно. Спасибо [Untraceable](https://twitter.com/DontTraceMeBruh) за то, что снова обратил на это внимание. Как было сказано, видео можно посмотреть ниже.

{{< youtube id="8quGD9W7B2I" autoplay="false" >}}  

![02](/img/post/2022-06-02-the-monero-moon-45/02.png)  

[SChernykh](https://github.com/SChernykh) опубликовал версию v2.1 P2Pool. Был внесён ряд изменений. Так сервер Stratum, например, теперь использует автоматическую настройку сложности по умолчанию, а обработка случаев отключения от интернета стала более надёжной, так как после обновления сервер полностью восстанавливается после любого длительного отключения. Обновление можно скачать [здесь](https://github.com/SChernykh/p2pool/releases/tag/v2.1).

![03](/img/post/2022-06-02-the-monero-moon-45/03.png)  
*https://github.com/SChernykh/p2pool/releases/tag/v2.1*

Вышла версия v5 PiNodeXMR! Согласно заявлениям команды PiNode, эта версия наиболее близка к Monero OS для одноплатных компьютеров. Это свободное программное обеспечение с открытым исходным кодом, поддерживающее Tor и I2P, P2Pool, блокчейн-эксплорер и многие другие удобные для новичков функции. По сути, PiNode-XMR позволит в режиме 24/7 поддерживать собственный полный или обрезанный узел на устройстве с низким энергопотреблением и приватно тратить XMR с помощью собственного узла, которому вы можете доверять. Более полную информацию можно найти [здесь](https://pinode.co.uk/) и [здесь](https://www.reddit.com/r/Monero/comments/v0y16n/pinodexmr_v5_out_now_the_closest_thing_to_a/).

![04](/img/post/2022-06-02-the-monero-moon-45/04.png)  
*https://pinode.co.uk/*

DangerousFreedom1984 поделился новостями о своей работе по разработке инструментов Python для проверки уровня инфляции в Monero и соответствующих учебных материалов. DangerousFreedom1984 утверждает, что до сего момента не нашёл никаких ошибок, которые могли бы привести к инфляции. Чтобы узнать обо всём более подробно, перейдите по [этой ссылке](https://www.reddit.com/r/Monero/comments/v21n4j/ccs_update_monero_inflation_checker/).

![05](/img/post/2022-06-02-the-monero-moon-45/05.png)  
*https://www.moneroinflation.com/*

Команда Monero Talk опубликовала видео с конференции Monerotopia с участием Ли Клагетта (Lee Clagett), также известного как VTnerd, разработчика Monero и эксперта в вопросах p2p сети XMR. Ли поделился своими мыслями относительно важности P2P-шифрования в Monero.

{{< youtube id="c1S7U8WCVgg" autoplay="false" >}}  

Любимый дедушка Monero, CryptoGrampy, создал альфа-версию торговой точки Monero под названием HotShop. Обратите внимание, что это пока только альфа-версия, и пользоваться ей следует исключительно с помощью тестовых сумм и тестовых кошельков. Если вы сможете помочь в тестировании программного обеспечения и сообщить о результатах дедуле Grampy, прежде чем он умрёт от старости, будет просто здорово. Более подробную информацию о торговой точке HotShop можно найти [здесь](https://www.reddit.com/r/Monero/comments/v0tvff/hotshop_ccs_milestones_1_2/).

{{< youtube id="jdupXaYY3po" autoplay="false" >}}  

Spirobel создал репозиторий для сбора скриптов, которыми можно воспользоваться, чтобы поиграть с monero-wallet-rpc! Подробности изложены в твите ниже.

![06](/img/post/2022-06-02-the-monero-moon-45/06.png)  

Seth For Privacy опубликовал [руководство](https://sethforprivacy.com/guides/accepting-monero-via-btcpay-server/) по приёму платежей Monero через сервер BTCPay. Руководство можно найти [здесь](https://sethforprivacy.com/guides/accepting-monero-via-btcpay-server/).

![07](/img/post/2022-06-02-the-monero-moon-45/07.png)  
*https://sethforprivacy.com/guides/accepting-monero-via-btcpay-server/*

Aki Mayumi на своём сайте выложил в доступ версию v1.2.1 мобильного кошелька Shruum v1.2.1. Об этом и говорится в твите, который приводится ниже.

![08](/img/post/2022-06-02-the-monero-moon-45/08.png)  

UnstoppableSwap объявили, что планируют продолжить разработку атомных свопов BTC-XMR и соответствующего GUI-приложения. Разработчик UnstoppableSwap, Binarybaron, пояснил, что всё строится на базе [swap-cli](https://github.com/comit-network/xmr-btc-swap/blob/master/docs/cli/README.md), в результате чего даже не обладающие специальными техническими знаниями пользователи смогут обменивать свои BTC на XMR безопасным, децентрализованным и не требующим доверия способом. Они также разместили в CCS запрос о финансировании, которое поспособствует разработке. Вся дополнительная информация содержится в этом [посте](https://www.reddit.com/r/Monero/comments/v072o3/soloptxmr_minimum_viable_product_1st_milestone/).

Mjxmr также поделился новостями о своём проекте SolOptXMR (Solar Optimal mining of XMR), целью которого является создание программного обеспечения с открытым исходным кодом, которое позволит людям заниматься майнингом Monero с помощью избыточной солнечной энергии. Mjxmr сообщил сообществу о завершении начального, подготовительного этапа. Более подробную информацию можно найти по этой ссылке.

![09](/img/post/2022-06-02-the-monero-moon-45/09.png)  
*https://www.reddit.com/r/Monero/comments/v072o3/soloptxmr_minimum_viable_product_1st_milestone/*

HackerIndustrial предлагает разработать специфичный форк Monero для SeedSigner под названием Monerosigner. Monerosigner будет представлять собой аппаратный кошелек с возможностью подписания транзакций офлайн и будет построен на базе Raspberry Pi Zero SBC. HackerIndustrial планирует реализовать форк кодовой базы, удалить компоненты Bitcoin, заменив их компонентами / специфическими функциями, обеспечивающими приватность Monero. Подробнее об этом читайте [здесь](https://www.reddit.com/r/Monero/comments/v2b3f6/ccs_proposal_monerosigner_fork_of_seedsigner_for/).

[CryptoMorpheus](https://www.reddit.com/user/CryptoMorpheus_/) опубликовал целый ряд новых графиков на сайте [monerujo.net](http://monerujo.net/)! Среди них показатели доминирования XMR и развития субреддита Monero. Более подробная информация содержится в [этом посте](https://monero.observer/cryptomorpheus_-builds-10-new-moneroj-charts/).

![10](/img/post/2022-06-02-the-monero-moon-45/10.png)  
*https://moneroj.net/social6/*

[The Monero Observer](https://www.monero.observer/) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://monero.observer/monero-dev-activity-report-week-21-2022/).

![11](/img/post/2022-06-02-the-monero-moon-45/11.png)  
*https://monero.observer/monero-dev-activity-report-week-21-2022/*

1 июня состоялась встреча Исследовательской лаборатории Monero. Среди прочего обсуждались алгоритмы мультиподписи и выбора ложных выходов. Соответствующие ссылки и дополнительную информацию по этой встрече можно найти [здесь](https://monero.observer/monero-research-lab-meeting-1-june-2022/#fn:14). Благодарим за это The Monero Observer! Встречи лаборатории MRL обычно проходят в 17:00 UTC на IRC-канале #monero-research-lab. Заглядывайте, если вам интересно, и увидите всё сами в режиме реального времени.

### _Прочие новости_

Midipoet выступил представителем сообщества Monero на Oslo Freedom Forum, ежегодной конференции по правам человека, проводимой Фондом защиты прав человека и в значительной степени ориентированной на Bitcoin. Его отчет по итогам конференции можно найти [здесь](https://www.reddit.com/r/Monero/comments/v18o78/ccs_report_midipoet_at_the_oslo_freedom_forum/).

Команда Cake Wallet, мобильного кошелька, который изначально был исключительно кошельком Monero, теперь является спонсором подкаста What Bitcoin Did. Соответствующее объявление содержится в твите ниже, где также рекомендуется использовать Monero в качестве средства для оплаты личных расходов!

![12](/img/post/2022-06-02-the-monero-moon-45/12.png)  

AMBcrypto опубликовал статью под заголовком «Сможет ли Monero [XMR] отыграть на фоне восстановления более глобальных настроений в отношении криптовалюты» (Will Monero [XMR] be able to rally amid recovering broader crypto sentiments). Полный текст статьи можно найти по этой [ссылке](https://ambcrypto.com/will-monero-xmr-be-able-to-rally-amid-recovering-broader-crypto-sentiments/).

![13](/img/post/2022-06-02-the-monero-moon-45/13.png)  
*https://ambcrypto.com/will-monero-xmr-be-able-to-rally-amid-recovering-broader-crypto-sentiments/*

Monero Talk взяли интервью у Нама Сардара (Nam Sardar), основателя Need Capital и сторонника Monero. Даг и Нам обсудили важность цифровых денег и почему Нам считает Monero наилучшим кандидатом на то, чтобы стать настоящей валютой в цифровую эпоху.

{{< youtube id="FOwzq-9uPHo" autoplay="false" >}}  

Monero Talk также опубликовали видео с конференции Monerotopia, в котором Генри, генеральный директор Techlore, рассказывает о создании удобных инструментов, необходимых для обеспечения приватности.

{{< youtube id="t-gaJ3y2OJ0" autoplay="false" >}}  

hoiru, создатель [iseeyour.cash](https://iseeyour.cash/), объявил о запуске сайта [moneroj.info](https://moneroj.info/), где будет делиться знаниями и полезными статьями о Monero с новичками и неопытными в техническом плане людьми. Более подробную информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/uyvelj/introducing_monerojinfo/).

![14](/img/post/2022-06-02-the-monero-moon-45/14.png)  
https://moneroj.info/

На канале [LoveraTV](https://www.youtube.com/c/BTCLovera) появилось новостное видео для испаноязычных членов сообщества Monero. Видео можно посмотреть на YouTube с английскими субтитрами.

{{< youtube id="4OYQuaTJ7WQ" autoplay="false" >}}  

На Miro, популярной онлайн-платформе для совместной работы, появилась иконка Monero.

![15](/img/post/2022-06-02-the-monero-moon-45/15.png)  
*https://www.reddit.com/r/Monero/comments/uz6xj5/found_the_monero_logo_in_miros_builtin_icon_set/*

Вышли новые выпуски еженедельных новостных дайджестов [The Monero Standard №15](https://localmonero.co/the-monero-standard/weekly/15) и [Revuo Monero №122](https://revuo-xmr.com/issue-122.html)! Читайте самые последние новости Monero, но не забывайте о The Monero Moon!

escapethe3RA из [monero.observer](https://monero.observer/) опубликовал [Monero Observer Blitz №10](https://monero.observer/monero-observer-blitz-may-2022/) за май 2022. В выпуске подводится итог всему произошедшему в сообществе Monero в мае этого года. Луковая ссылка опубликована [здесь](https://www.reddit.com/r/Monero/comments/v2wtz4/monero_observer_blitz_10_may_2022/).

![16](/img/post/2022-06-02-the-monero-moon-45/16.png)  
https://monero.observer/monero-observer-blitz-may-2022/

melon_crust работает над созданием веб-сайта, который поможет людям узнать буквально всё о Monero. Заходите на [learnmonero.co](https://learnmonero.co/)!

![17](/img/post/2022-06-02-the-monero-moon-45/17.png)  
*learnmonero.co*

### _Мероприятия_

8 июня в Нью-Йорке, Колорадо, Лас-Вегасе, Чикаго и других местах состоится Глобальное празднование (встреча по поводу) дня начала постэмиссии. Вы также можете отпраздновать окончание номинальной эмиссии Monero и начало постэмиссии со своим местным сообществом XMR! Вы даже можете организовать собственную встречу в своём городе! Всю дополнительную информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/). Свяжитесь с @[chowbungaman](https://www.reddit.com/u/chowbungaman/) через [Telegram-канал Monerotopia](https://t.me/monerotopia) или через Matrix, если хотите организовать собственную встречу или присоединиться к организованной другими. Вы также можете связаться с ними по электронной почте: [monerotopia@protonmail.com](mailto:monerotopia@protonmail.com).

![18](/img/post/2022-06-02-the-monero-moon-45/18.png)  
*https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/*

Очередная плановая встреча по проведению MoneroKon 2022 состоится в субботу, 4 июня 2022 года, в 18:00 UTC на IRC-канале #monero-events.

![19](/img/post/2022-06-02-the-monero-moon-45/19.png)  
*https://monerokon.com/*

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если же вы хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Следует отметить, что билеты на Monerokon 2022 уже распроданы, но могут появиться дополнительные билеты.

Организаторы Monerokon также ищут волонтеров, которые могли бы помочь с решением ряда задач на конференции. Так что, если вы готовы протянуть руку помощи, свяжитесь с ними, перейдя по [этой ссылке](https://www.reddit.com/r/Monero/comments/v0vsqa/monerokon_2022_call_for_volunteers_it_takes_a/).

![20](/img/post/2022-06-02-the-monero-moon-45/20.png)  
*https://cryptpad.disroot.org/form/#/2/form/view/RqXzBJnXRsLaSBA6cMdtU0+45fXUvWDhXxxTOF1WM+A/embed/*

Majestic Labs, криптовалютная биржа, ориентированная на обеспечение приватности пользователей, и проект Monero объявили, что бесплатно раздадут 40 билетов на Monerokon. Всё, что вам нужно сделать, связаться с ними и объяснить, почему, по вашему мнению, именно вы должны побывать там. Вся дополнительная информация содержится в [этом посте](https://www.reddit.com/r/Monero/comments/uzvwsj/time_to_chill_with_fluffypony_free_monerokon/).

![21](/img/post/2022-06-02-the-monero-moon-45/21.png)  
*https://majesticbank.sc/*

### _Биржи и предприниматели_

Coincards вновь [сообщают](https://twitter.com/CoinCards/status/1532051778757201920?s=20&t=wIE3cHR5c396GaWNfl-iZA) о росте глобального использования Monero на своих сервисах. В процентном выражении этот показатель вырос с 20% до 25%, и Monero уступает только Bitcoin. Monero также является наиболее используемой на Coincards валютой в США, где её доля составляет целых 44%.

![22](/img/post/2022-06-02-the-monero-moon-45/22.png)  

Теперь у нас есть возможность покупать и продавать Monero за фиатные валюты, включая USD, EUR, CAD и GBP. Сделать это можно на сайте Monero.com.

![23](/img/post/2022-06-02-the-monero-moon-45/23.png)  

Для тех, кто хочет потратить XMR, был разработан новый сервис под названием FiatRefill. FiatRefill — это онлайн-платформа, позволяющая тратить криптовалюту абсолютно в любом интернет-магазине! Всю дополнительную информацию вы найдёте на их [веб-сайте](https://www.fiatrefill.com/).

![24](/img/post/2022-06-02-the-monero-moon-45/24.png)  
*https://www.fiatrefill.com/*

Если у вас имеются Nano, вы сможете обменять их на Monero, воспользовавшись услугами криптовалютного обменника Kuyumcu. Перед тем как пользоваться сервисом, пожалуйста, прочитайте раздел FAQ и узнайте, каковы минимально и максимально допустимые суммы транзакций ими поддерживаются.

![25](/img/post/2022-06-02-the-monero-moon-45/25.png)  
*https://monero.nano.trade/*

OrangeFrem.com, веб-сайт, на котором сравниваются ставки на биржах, предлагающих мгновенный обмен без KYC, предлагает своим клиентам воспользоваться гарантией OrangeFren. Гарантия OrangeFren заключается в том, что ресурс вернёт вам ваши деньги, если они будут украдены, если вы вынужденно утратите приватность и вам придётся следовать правилу KYC или если курс обмена, заявляемый биржей, по факту окажется иным! Подробности вы найдёте в этом посте.

![26](/img/post/2022-06-02-the-monero-moon-45/26.png)  
*Гарантия OrangeFren: https://www.reddit.com/r/Monero/comments/v2kygw/orangefren_guarantee_got_scammed_ill_refund_you/*

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![27](/img/post/2022-06-02-the-monero-moon-45/27.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![28](/img/post/2022-06-02-the-monero-moon-45/28.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![29](/img/post/2022-06-02-the-monero-moon-45/29.png)  
*https://ccs.getmonero.org/funding-required/*

Кроме того, премию в размере 5 XMR получит тот, кто поможет исправить неполадки с веб-сайтом для сбора пожертвований [Monero Bounties](https://bounties.monero.social/). Более подробную информацию можно узнать, ознакомившись с [этим постом](https://www.reddit.com/r/Monero/comments/uny2xi/bounty_to_fix_monero_bounties_site/).

### _Торговля и биржевые спекуляции_

Говоря о паре XMR/BTC, можно констатировать, что Monero официально вырвалась из четырёхлетнего нисходящего тренда по отношению к Bitcoin, и месячная свеча закрылась выше уровня сопротивления. Быки могут надеяться, что соотношение будет расти. Откат назад и повторный анализ примерно на уровне ~0,0059 BTC были бы разумным исходом.

![30](/img/post/2022-06-02-the-monero-moon-45/30.png)  

В течение последних четырех месяцев доминирование Monero по общей криптовалютной рыночной капитализации только укрепляется.

![31](/img/post/2022-06-02-the-monero-moon-45/31.png)  

С середины декабря 2021 года Monero демонстрирует тенденцию к росту по отношению к Ethereum, устанавливая всё более высокие минимумы на протяжении более чем 5 месяцев.

![32](/img/post/2022-06-02-the-monero-moon-45/32.png)  

Trade Ogre отметили поступление крупных заявок на покупку XMR в течение последних дней. 30 мая кто-то обменял более 120 BTC на более чем 19 000 XMR, разместив на Trade Ogre всего одну крупную заявку. Вначале цена на «стене закупки» составляла 0,00645 BTC, а затем была сдвинута до 0,0066, чтобы гарантировать, что заказ будет заполнен. Спасибо 1centarmy за то, что привлёк к этому общее внимание.

![33](/img/post/2022-06-02-the-monero-moon-45/33.png)  
https://twitter.com/1centarmy

Пользователь Twitter под ником Ergo утверждает, что покупатель XMR на Trade Ogre пользуется флэш-кредитами Cream.

![34](/img/post/2022-06-02-the-monero-moon-45/34.png)  

Разработчик программного обеспечения Чад Тэккерей (Chad Thackray) недавно выступил на конференции Monerotopia по вопросу ценового профиля Monero и объяснил, почему он имеет значение. Видео можно посмотреть ниже.

{{< youtube id="05W1lrhY1S0" autoplay="false" >}}  

[without_worries](https://www.tradingview.com/u/without_worries/) [прогнозирует](https://www.tradingview.com/chart/XMRUSD/LhKZaeQk-Monero-XMR-to-4000/), что к концу 2023 года цена Monero вырастет до 4000 USD.

![35](/img/post/2022-06-02-the-monero-moon-45/35.png)  
https://www.tradingview.com/chart/XMRUSD/LhKZaeQk-Monero-XMR-to-4000/

_**Показатели**_
- Общее количество Monero в обращении: 18 129 242 XMR
- Общая рыночная капитализация Monero: 3 306 789 322 USD
- Позиция в рейтенге Coinmarketcap: 25
- Цена XMR/USD: ~195 USD
- Цена XMR/BTC: 0.00650 BTC
- Цена на LocalMonero.co: 225 USD
- Средний размер комиссии за проведение транзакции: 0.00012 XMR ($0.022)
- Хешрейт: 2.877 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![36](/img/post/2022-06-02-the-monero-moon-45/36.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![37](/img/post/2022-06-02-the-monero-moon-45/37.png)  
*https://www.reddit.com/r/Monero/comments/uxzmu5/shoutout_from_northern_new_mexico/*

![38](/img/post/2022-06-02-the-monero-moon-45/38.png)  
*Keep Your Fiat, I Want Monero. /Sidarta0 - https://www.reddit.com/r/Monero/comments/v0k3z9/keep_your_fiat_i_want_monero_sidarta0/*

![39](/img/post/2022-06-02-the-monero-moon-45/39.png)  
*Use Monero - Urban Diaries https://www.twitter.com/AGNFAB1/status/1529736172217548801/photo/1*

![40](/img/post/2022-06-02-the-monero-moon-45/40.png)  
*https://www.reddit.com/r/monerochan/comments/n1v350/monerochan/*

![41](/img/post/2022-06-02-the-monero-moon-45/41.png)  
*https://i.redd.it/mbkl57zy5a291.jpg*

![42](/img/post/2022-06-02-the-monero-moon-45/42.png)  
*https://www.reddit.com/r/moonero/comments/uuy1tm/nothing_else_matters/*

![43](/img/post/2022-06-02-the-monero-moon-45/43.png)  

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 45)](https://www.themoneromoon.com/p/the-monero-moon-issue-45?s=r)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
