---
title: "The Monero Moon (выпуск 43)"
date: "2022-05-19"
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

16 июля 2022 года на высоте блока 2 668 888 состоится согласованное сообществом Monero обновление сети (хардфорк), призванное повысить уровень приватности и общей производительности. Всем пользователям необходимо обновить программное обеспечение. Новая версия v0.18 Fluorine Fermi будет опубликована за месяц до сетевого обновления, то есть примерно 16 июня. В рамках обновления будет реализован целый ряд новых функций, среди прочего:
- размер кольца будет увеличен с 11 до 16 в целях повышения приватности;
- будут реализованы теги просмотра, в результате чего время синхронизации сократится на 40%;
- после введения Bulletproofs+ размер транзакций уменьшится примерно на 7%, равно как и время верификации, которое также сократится на 7%.

Также вместе с новым программным обеспечением вскоре будет опубликован полный список улучшений и усовершенствований. Если вы хотите узнать больше о грядущем обновлении сети Monero, пожалуйста, ознакомьтесь с [этим постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html) на официальном [веб-сайте Monero](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html). Вы также можете прочитать [журнал встречи](https://github.com/monero-project/meta/issues/684) разработчиков Monero, состоявшейся 16 апреля, на которой обсуждалось данное обновление сети.

![01](/img/post/2022-05-19-the-monero-moon-43/01.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*

Если вы желаете помочь с обновлением сети Monero, достаточно просто уведомить о нём провайдеров кошельков и биржевых сервисов. Пожалуйста, сверьтесь с этим [контрольным листом](https://github.com/monero-project/meta/issues/690), чтобы все надлежащим образом обновили своё программное обеспечение и внесли соответствующие изменения.

![02](/img/post/2022-05-19-the-monero-moon-43/02.png)  
*https://github.com/monero-project/meta/issues/690*

Кроме того, вы можете помочь в тестировании и выявить ошибки в основной версии протокола Monero. Сделать это можно в тестовой сети. Соответствующие тестовые средства (tXMR) доступны абсолютно любому желающему! Дополнительную информацию, связанную с возможным оказанием помощи, можно найти в [этом посте, опубликованном garth_xmr](https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/).

![03](/img/post/2022-05-19-the-monero-moon-43/03.png)  
*https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/*

P2Pool продолжает демонстрировать невероятный рост. Так недавно пул насчитывал уже 1500 активных майнеров. Разработчик Monero sech1 поделился с сообществом информацией, согласно которой, благодаря недавно вышедшей [версии GUI Monero](https://www.getmonero.org/downloads/#gui), в которой была добавлена поддержка [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html), P2Pool-mini на данный момент насчитывает более 1000 активных майнеров (в сравнении с 300 майнерами 2 недели назад). Призываем всех поддержать сеть Monero, создав собственный узел!

![04](/img/post/2022-05-19-the-monero-moon-43/04.png)  
*https://www.reddit.com/r/Monero/comments/urh3oe/p2pool_is_growing/*

[Schernykh](https://github.com/SChernykh) создал в тестовой сети P2Pool, чтобы убедиться в том, что всё будет работать, как положено, после сетевого обновления. [Тестирование прошло без каких-либо проблем](https://github.com/SChernykh/p2pool/issues/153).

DragonSided-D поделился простым руководством по созданию узла Monero. Руководство можно найти [здесь](https://www.reddit.com/r/Monero/comments/upnjyo/comment/i8m7ps1/?utm_source=share&utm_medium=web2x&context=3).

![05](/img/post/2022-05-19-the-monero-moon-43/05.png)  
*https://www.reddit.com/r/Monero/comments/upnjyo/comment/i8m7ps1/?utm_source=share&utm_medium=web2x&context=3*

mWo12 поделился предварительным вариантом того, как будут выглядеть блокчейн-эксплореры Monero после июльского обновления сети.

![06](/img/post/2022-05-19-the-monero-moon-43/06.png)  
*https://www.reddit.com/r/Monero/comments/up4ac2/preview_of_upcoming_v15_monero_network_update/*

Команда Cake Wallet на Monero.com добавила множество крутых [графиков Monero](https://monero.com/charts/shielded), включая графики, демонстрирующие ежемесячный рост количества транзакций в сравнении с другими ориентированными на обеспечение приватности монетами/технологиями, а также модель отношения запасов к производимым Monero. Это было сделано подобно тому, как публикуется на [Moneroj.net](https://moneroj.net/).

![07](/img/post/2022-05-19-the-monero-moon-43/07.png)  
*https://monero.com/charts/shielded*

В рамках обновления сети Monero будет реализована функция под названием «теги просмотра», которая позволит сократить время синхронизации кошельков на 40%. Интересно, что такое теги просмотра? Тогда читайте [этот пост](https://localmonero.co/knowledge/view-tags-reduce-monero-sync-time?language=en), опубликованный на LocalMonero. Если же вам требуется просто объяснение, посмотрите этот [развлекательный мультфильм](https://moneroworld.com/viewtag_cartoon.html), размещённый Gingeropolous, в котором разъясняется, что такое теги просмотра.

![08](/img/post/2022-05-19-the-monero-moon-43/08.png)  
*https://moneroworld.com/viewtag_cartoon.html*

[The Monero Observer](https://www.monero.observer/) опубликовали очередной отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://www.monero.observer/monero-dev-activity-report-week-19-2022/).

Команда Monerujo на f-droid alpha и на GitHub опубликовала новую минимальную бета-версию, соответствующую обновлению до версии Monero Core v0.17.3.2 с поддержкой Ledger Nano S plus!

![09](/img/post/2022-05-19-the-monero-moon-43/09.png)  

Вышла версия v1.1.1 Shruum Wallet, форка Monerujo, с дополнительными возможностями обеспечения безопасности, достигаемыми за счёт добавления и удаления некоторых функций. Обновление можно найти [здесь](https://www.reddit.com/r/Monero/comments/uqzbx3/shruum_wallet_v111_monero_01732_bug_fixes_a_new/)!

Команда Cake Wallet нанимает и ищет разработчиков! Более подробную информацию можно найти в [этом посте](https://www.linkedin.com/jobs/view/3072597005).

Команда децентрализованной биржи Haveno делится новостями о своей работе!

![10](/img/post/2022-05-19-the-monero-moon-43/10.png)  
*https://haveno.exchange/blog/updates2/*

ForgotSudo, занимающийся разработкой децентрализованной торговой площадки Monero, также опубликовал новости о своей деятельности. Более подробную информацию можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/urby44/monero_decentralized_marketplace_brief_update/).

Koe разместил в системе CCS предложение по дальнейшей работе над Seraphis. С предложением можно ознакомится [здесь](https://ccs.getmonero.org/proposals/seraphis-wallet-poc-2.html).

[jeffro256](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/319) также желает поработать над Monero, улучшить алгоритм выбора узлов и так усовершенствовать GUI, чтобы люди не платили слишком больших комиссий, взымаемых вредоносными узлами.

Оказывается, [Google поддерживает Monero](https://github.com/google/oss-fuzz/tree/master/projects/monero) посредством своего сервиса Assured Open Source Software.

![11](/img/post/2022-05-19-the-monero-moon-43/11.png)  
*https://github.com/google/oss-fuzz/tree/master/projects/monero*

Monero Talk опубликовали запись с конференции Monerotopia, полностью посвящённую Monero и квантовым вычислениям. Это выступление Адама Корбо (Adam Corbo), физика и криптографа, интересующегося проблемой квантовых вычислений, в котором он рассуждает о проведении постквантового аудита лабораториями Monero и будущем блокчейн-технологии в парадигме постквантовых вычислений.

{{< youtube id="rGae-vCD_Vo" autoplay="false" >}}  

### _Прочие новости_

Exodus Wallet опубликовали статью, посвящённую Monero, под названием [Обновление Monero XMR 2022](https://www.exodus.com/news/monero-xmr-update-2022/). Статья довольно подробная и стоит прочтения.

![12](/img/post/2022-05-19-the-monero-moon-43/12.png)  
*https://www.exodus.com/news/monero-xmr-update-2022/*

Stoic HODLer в своём блоге опубликовал статью под названием «CBDC наступают... почему приватность денег нельзя игнорировать» (CBDC’s are coming… Why Privacy is NOT NEGOTIABLE in money). Статью можно найти по [этой ссылке](https://stoichodler.substack.com/p/cbdcs-are-coming-why-privacy-is-not?sd=nfs&s=r).

Команда Monero Talk также поделилась видео с конференции Monerotopia с выступлением Филиппа Циммермана (Philip Zimmermann), изобретателя PGP (программы шифрования Pretty Good Privacy), в котором он делится своими мыслями о сохранении демократии с помощью криптографии.

{{< youtube id="a4nOQCXVOzc" autoplay="false" >}}  

Если вы испаноговорящий сторонник Monero, посмотрите видео, размещённое ниже.

{{< youtube id="0Y0jgO0PXoY" autoplay="false" >}}  

The Monero Observer, прекрасный источник новостей, связанных с Monero, информирует сообщество о том, что является на 100% открытым проектом.

![13](/img/post/2022-05-19-the-monero-moon-43/13.png)  
*https://www.reddit.com/r/Monero/comments/upsmgy/monero_observer_is_100_open_source_content_and/*

Разработчик Firo поделился своим мнением относительно преимуществ постэмиссии, которая, на его взгляд, обеспечит безопасность сети в будущем.

![14](/img/post/2022-05-19-the-monero-moon-43/14.png)  

Немного в отрыве от Monero в Сальвадоре прошла встреча, на которой обсуждались криптовалюты и их место в финансовой сфере в рамках цифровых экономик.

![15](/img/post/2022-05-19-the-monero-moon-43/15.png)  

### _Мероприятия_

Постэмиссия Monero уже не за горами. Она начнётся на высоте блока 2 641 623 примерно 8 июня. Интересуетесь, что такое постэмиссия и почему она так важна для успеха Monero в будущем? Тогда смотрите скриншот, размещённый ниже, а также ознакомьтесь с постами, опубликованными [здесь](https://www.getmonero.org/resources/moneropedia/tail-emission.html) и [здесь](https://localmonero.co/knowledge/monero-tail-emission?language=en).

![16](/img/post/2022-05-19-the-monero-moon-43/16.png)  
*https://www.getmonero.org/resources/moneropedia/tail-emission.html*

![17](/img/post/2022-05-19-the-monero-moon-43/17.png)  

{{< youtube id="8quGD9W7B2I" autoplay="false" >}}  

8 июня в Нью-Йорке, Колорадо, Лас-Вегасе и Чикаго состоится Глобальное празднование (встреча по поводу) дня начала постэмиссии. Вы также можете отпраздновать окончание номинальной эмиссии Monero и начало постэмиссии со своим местным сообществом XMR! Вы даже можете организовать собственную встречу в своём городе! Всю дополнительную информацию можно найти по этой ссылке.

![18](/img/post/2022-05-19-the-monero-moon-43/18.png)  
*https://www.reddit.com/r/Monero/comments/ummf0v/nyc_monero_tail_emission_day_global_meet_up/*

![19](/img/post/2022-05-19-the-monero-moon-43/19.png)  

Очередная плановая встреча по проведению конференции MoneroKon 2022 состоится в субботу, 21 мая 2022 года в 18:00 UTC на IRC-канале #monero-events.

Билеты на конференцию Monerokon распроданы!

![20](/img/post/2022-05-19-the-monero-moon-43/20.png)  
*https://monerokon.com/products/monerokon2022*

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Билеты на MoneroKon теперь можно приобрести [здесь](https://monerokon.com/products/monerokon2022), на веб-сайте MoneroKon.

![21](/img/post/2022-05-19-the-monero-moon-43/21.png)  
*https://monerokon.com/*

### _Биржи и предприниматели_

Binance теперь поддерживает XMR как залоговый актив на платформе Binance Loans. До этого Binance обвиняли в частичном резервировании XMR, поэтому сообщество Monero довольно резко встретило эту новость.

![22](/img/post/2022-05-19-the-monero-moon-43/22.png)  
*https://www.binance.com/en/support/announcement/a0bd5f2e306147bb9c7e0c0c72852251*

Если вдруг пропустили, обязательно посмотрите видео выступления Рольфа Ван Вегберга (Rolf van Wegberg) на Monerotopia, посвящённого рынкам даркнета и Monero.

{{< youtube id="_1gdNLogVWM" autoplay="false" >}}  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![23](/img/post/2022-05-19-the-monero-moon-43/23.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![24](/img/post/2022-05-19-the-monero-moon-43/24.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![25](/img/post/2022-05-19-the-monero-moon-43/25.png)  
*https://ccs.getmonero.org/funding-required/*

Кроме того, премию в размере 5 XMR получит тот, кто поможет исправить неполадки с веб-сайтом для сбора пожертвований [Monero Bounties](https://bounties.monero.social/). Более подробную информацию можно узнать, ознакомившись с [этим постом](https://www.reddit.com/r/Monero/comments/uny2xi/bounty_to_fix_monero_bounties_site/).

### _Торговля и биржевые спекуляции_

Пара XMR/USD отскочила от 200-дневной скользящей средней (показана оранжевой линией), но не попала в бычий тренд, продолжавшийся последние четыре недели.

![26](/img/post/2022-05-19-the-monero-moon-43/26.png)  

[CryptoBullet](https://www.tradingview.com/chart/XMRUSD/hxtUkdex-Market-Cycles-XMR-as-an-example/) полагает, что падение продолжится, после чего XMR снова пойдёт вверх.

![27](/img/post/2022-05-19-the-monero-moon-43/27.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 123 027 XMR
- Общая рыночная капитализация Monero: 2 826 717.789 USD
- Позиция в рейтенге Coinmarketcap: 30
- Цена XMR/USD: ~156 USD
- Цена XMR/BTC: 0.00535 BTC
- Цена на LocalMonero.co: 174 USD
- Средний размер комиссии за проведение транзакции: 0.00011 XMR ($0.017)
- Хешрейт: 2.948 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![28](/img/post/2022-05-19-the-monero-moon-43/28.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![29](/img/post/2022-05-19-the-monero-moon-43/29.png)  
*SpySTAFFO15 typed Monero on an AI art maker - https://www.reddit.com/r/Monero/comments/uq3efv/typed_monero_on_an_ai_art_maker/*

![30](/img/post/2022-05-19-the-monero-moon-43/30.png)  
*https://www.reddit.com/r/moonero/comments/m4txd7/always_improving/*

![31](/img/post/2022-05-19-the-monero-moon-43/31.png)  
*https://www.reddit.com/r/moonero/comments/iqc0zf/newb_use_of_monero_is_more_private_than_ninja_use/*

![32](/img/post/2022-05-19-the-monero-moon-43/32.png)  
*https://www.reddit.com/r/moonero/comments/qrrksp/we_are_waiting/*

![33](/img/post/2022-05-19-the-monero-moon-43/33.png)  
*https://www.reddit.com/r/moonero/comments/7g78az/not_too_early_and_not_too_late/*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 43)](https://www.themoneromoon.com/p/the-monero-moon-issue-43?s=r)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
