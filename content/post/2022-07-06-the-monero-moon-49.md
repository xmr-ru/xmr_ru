---
title: "The Monero Moon (выпуск 49)"
date: "2022-07-06"
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

Разработчиками было [принято решение](https://monero.observer/monero-hard-fork-rescheduled-13-august-2022/) отложить обновление сети Monero (хардфорк) примерно на две недели из-за задержки, связанной с аудитом multisig, проводимым третьей стороной. Срок перенесён на 13 августа 2022 г. Обновление сети состоится на высоте блока 2 688 888 вместо ранее заявленной высоты 2 668 888, то есть на двадцать тысяч блоков позднее (ранее предлагалось произвести обновление на высоте блока 2 678 888).

![01](/img/post/2022-07-06-the-monero-moon-49/01.png)  
*https://monero.observer/assets/logs/220630-dev.log*

Запланированное обновление сети Monero (хардфорк) является обновлением, согласованным сообществом Monero, призванным повысить уровень приватности и общей производительности. Всем пользователям необходимо обновить программное обеспечение. Программное обеспечение, которое будет необходимо установить в целях обеспечения соответствия обновлению сети, выйдет 13 июля (v0.18 Flourine Fermi). У всех пользователей будет две недели, чтобы осуществить переход. Если вы пользуетесь мобильным кошельком или каким-либо сторонним приложением, убедитесь в том, что у вас установлена актуальная версия. Если у вас возникнут вопросы, пожалуйста, свяжитесь с членами сообщества Monero на канале r/Monero или с помощью другой социальной платформы.

В рамках обновления будет реализован целый ряд новых функций, среди прочего:
- размер кольца будет увеличен с 11 до 16 в целях повышения приватности;
- будут реализованы теги просмотра, в результате чего время синхронизации сократится на 40%;
- после введения Bulletproofs+ размер транзакций уменьшится примерно на 7%, равно как и время верификации, которое также сократится на 7%.

Также вместе с новым программным обеспечением вскоре будет опубликован полный список улучшений и усовершенствований. Если вы хотите узнать больше о грядущем обновлении сети Monero, пожалуйста, ознакомьтесь [с этим постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html) на официальном [веб-сайте Monero](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html).

![02](/img/post/2022-07-06-the-monero-moon-49/02.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*

Если вы желаете помочь с обновлением сети Monero, достаточно просто уведомить о нём провайдеров кошельков и биржевых сервисов. Пожалуйста, сверьтесь с этим [контрольным листом](https://github.com/monero-project/meta/issues/690), чтобы все надлежащим образом обновили своё программное обеспечение и внесли соответствующие изменения.

![03](/img/post/2022-07-06-the-monero-moon-49/03.png)  
*https://github.com/monero-project/meta/issues/690*

selsta поделился новостями о своей работе в качестве разработчика (частичная занятость). selsta работает на проект Monero начиная с 2018 г. На его счету более 525 включённых коммитов. Самые последние новости по разработке, осуществляемой selsta (за июнь 2022), можно найти [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/312#note_17037).

![04](/img/post/2022-07-06-the-monero-moon-49/04.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/312#note_17037*

[DangerousFreedom1984](https://github.com/DangerousFreedom1984) также опубликовал [отчёт](https://www.reddit.com/r/Monero/comments/vqm7bg/ccs_update_monero_inflation_checker_report_2/) по своей работе над инструментом для расчёта инфляции Monero (Monero Inflation Checker). Ошибок, которые могли бы вызвать инфляцию, выявлено не было. Полный текст отчёта по работе DangerousFreedom1984 можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/vqm7bg/ccs_update_monero_inflation_checker_report_2/).

![05](/img/post/2022-07-06-the-monero-moon-49/05.png)  
*https://www.moneroinflation.com/*

[ACK-J](https://github.com/ACK-J) тоже поделился новостями по своей работе, связанной с оценкой поверхности атаки кольцевых подписей при использовании технологии машинного обучения и глубокого обучения. Отчёт вместе с версией tldr можно найти [здесь](https://github.com/MAGICGrants/Monero-Fund/issues/15#issuecomment-1172972999).

![06](/img/post/2022-07-06-the-monero-moon-49/06.png)  
*https://github.com/MAGICGrants/Monero-Fund/issues/15#issuecomment-1172972999*

Exodus, криптовалютный кошелёк для самостоятельного кастодиального хранения, теперь поддерживает Monero при использовании с аппаратным кошельком Trezor, как ранее лично и обещал гендиректор Exodus. Более подробную информацию можно найти [здесь](https://www.reddit.com/r/ExodusWallet/comments/vokk8g/exodus_22630_mobile_and_2271_desktop_release/).

![07](/img/post/2022-07-06-the-monero-moon-49/07.png)  
*https://www.reddit.com/r/ExodusWallet/comments/vokk8g/exodus_22630_mobile_and_2271_desktop_release/*

![08](/img/post/2022-07-06-the-monero-moon-49/08.png)  

SChernykh выложил в доступ новую версию [P2Pool v2.2](https://github.com/SChernykh/p2pool/releases). Эта версия соответствует грядущему обновлению сети Monero до версии v15. Предшествующие версии p2pool будут несовместимы с ней. В версии 2.2 был реализован целый ряд обновлений и исправлены некоторые ошибки. Этот [пост](https://github.com/SChernykh/p2pool/releases) поможет вам с обновлением, а также позволит получить больше информации.

![09](/img/post/2022-07-06-the-monero-moon-49/09.png)  
*https://github.com/SChernykh/p2pool/releases*

На момент написания этого выпуска minexmr.com имел примерно 43% всего известного хешрейта. Несмотря на то, что MineXMR не являются какими-то злоумышленниками, занимающимися майнингом в сети Monero, майнерам настоятельно рекомендуется прекратить майнинг с помощью minexmr.com в целях поддержания децентрализованности глобальной сети. Список альтернативных пулов для майнинга можно найти по следующей ссылке: [miningpoolstats.stream/monero](https://miningpoolstats.stream/monero).

![10](/img/post/2022-07-06-the-monero-moon-49/10.png)  
*https://minexmr.com/pools.html*

Какой объём средств ежедневно передаётся по сети Monero? [Untraceable](https://twitter.com/DontTraceMeBruh/status/1543513471119138817) предлагает свою оценку в [твите](https://twitter.com/DontTraceMeBruh/status/1543513471119138817), опубликованном ниже.

![11](/img/post/2022-07-06-the-monero-moon-49/11.png)  

[bashkyc](https://www.reddit.com/user/bashkyc/) открыл [горячую линию поддержки](https://bashkyc.github.io/bashkyc-onionsite/) для тех, кто попал в неприятную ситуацию ([BASH -KYC](https://bashkyc.github.io/bashkyc-onionsite/)). Горячая линия представляет собой целое собрание кошельков, бирж и приватных инструментов, не следующих правилу KYC, предназначенных для таких криптовалют, как Monero. На официальный сайт можно попасть только с помощью Tor. Ссылки , которые можно использовать, чтобы зайти на веб-сайт через Clearnet и Tor, можно найти [здесь](https://www.reddit.com/r/Monero/comments/vt04gw/the_boating_accident_support_hotline_a_collection/).

![12](/img/post/2022-07-06-the-monero-moon-49/12.png)  
*https://bashkyc.github.io/bashkyc-onionsite/*

matejcik проинформировал сообщество Monero о том, что пользователи Trezor в течение четырёх дней будут сталкиваться со сбоями в работе сервиса. Более подробная информация содержится в этом посте.

![13](/img/post/2022-07-06-the-monero-moon-49/13.png)  
*https://github.com/monero-project/monero/pull/8299*

Monero Observer опубликовали директорию существующих подозрительных проектов экосистемы, которых следует избегать пользователям Monero. Также приводится соответствующая ссылка на подкрепляющие доказательства. Всю соответствующую информацию можно найти здесь. Если вы считаете, что какой-либо из сервисов следует исключить из списка, свяжитесь с [escapethe3RA](https://monero.observer/about).

![14](/img/post/2022-07-06-the-monero-moon-49/14.png)  
*https://monero.observer/blacklist/*

[Monero Observer](https://www.monero.observer/) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-26-2022/).

### _Прочие новости_

anarkio создал веб-страницу со ссылками и информацией, так или иначе связанной с Monero. Среди прочего, посетив страницу, вы узнаете, как купить и потратить Monero, как принимать XMR к оплате, если вы являетесь предпринимателем, а также найдёте ссылки, необходимые, чтобы связаться с сообществом, и многое другое. Перейти на страницу можно по [этой ссылке](https://anarkio.codeberg.page/monero/).

![15](/img/post/2022-07-06-the-monero-moon-49/15.png)  
*https://anarkio.codeberg.page/monero/*

Monero Observer опубликовали дайджест Monero Observer Blitz №11 за июнь 2022 г. В дайджесте кратко изложено всё то, что происходило в сообществе Monero в июне. Найти дайджест можно [здесь](https://monero.observer/monero-observer-blitz-june-2022/).

![16](/img/post/2022-07-06-the-monero-moon-49/16.png)  
*https://monero.observer/monero-observer-blitz-june-2022/*

Недавно Monero Talk взяли интервью у известного сторонника Bitcoin Брюса Фентона (Bruce Fenton) и Старра О'Хара, присутствовавших на Porcfest 2022. Посмотреть интервью можно ниже.

{{< youtube id="a5C8zMp-Ur0" autoplay="false" >}}  

Monero Talk также опубликовали эпизод №72 Monerotopia. В нём команда Monero Talk рассказала о своей недавней поездке на Porcfest 2022, поделилась отчётом по актуальным ценам, а также пообщалась со специальным гостем Mirage Sale, создавшим подобную eBay платформу, поддерживающую платежи в Monero!

{{< youtube id="2HNZdM0zJEQ" autoplay="false" >}}  

[Crypto Vigilante](https://www.youtube.com/c/CryptoVigilante) опубликовал [видео](https://www.youtube.com/watch?v=dV5fZf3Wru8) с Люком Смитом (Luke Smith), в котором говорится о том, как Monero поможет избежать дистопии. Видео можно посмотреть ниже.

{{< youtube id="dV5fZf3Wru8" autoplay="false" >}}  

Разработчик DarkFi Рейчел-Роуз О'Лири (Rachel-Rose O’Leary) приняла участие в шоу Джастина Мерфи (Justin Murphy) под названием Other Life. На вопрос, почему Monero лучше ZCash, она ответила, что Monero изначально поддерживается стихийным сообществом, и ежедневно проводится больше транзакций Monero, а не ZCash, который используют корпоративный подход с выплатой комиссий разработчикам. Послушать Рейчел-Роуз можно ниже или по [этой ссылке](https://www.youtube.com/watch?v=ya3CsbfnT_Y&t=773s).

{{< youtube id="ya3CsbfnT_Y" autoplay="false" >}}  

Джон Фосс (John Foss), да-да, это я, опубликовал твит под заголовком «Как Monero отбирает хлеб у Bitcoin, и ещё десять других вещей, которые вы не знали о Monero» (How Monero is Eating Bitcoin’s Lunch — And Ten Other Things You Didn’t Know About Monero). В твите охвачены самые разные показатели (объём транзакций, использование на Coincards, DNM и так далее), отражающие рост и доминирование Monero в сравнении с Bitcoin. Твит можно найти [здесь](https://twitter.com/johnfoss69/status/1542868844141678593).

![17](/img/post/2022-07-06-the-monero-moon-49/17.png)  

Seth For Privacy в режиме живого эфира в рамках своего подкаста Opt Out, посвящённого вопросам приватности, провёл сеанс вопросов и ответов. Запись можно посмотреть [здесь](https://www.youtube.com/watch?v=t9ZINjOtp7c) или ниже.

{{< youtube id="t9ZINjOtp7c" autoplay="false" >}}  

Опубликован восемнадцатый выпуск [The Monero Standard](https://localmonero.co/the-monero-standard/weekly/18).  Найти его можно [здесь](https://localmonero.co/the-monero-standard/), на веб-сайте LocalMonero.co!

![18](/img/post/2022-07-06-the-monero-moon-49/18.png)  
*https://localmonero.co/the-monero-standard/weekly/18*

Также вышел сто двадцать седьмой выпуск Revuo Monero. Ознакомиться с ним и узнать последние новости Monero можно по [этой ссылке](https://revuo-xmr.com/).

![19](/img/post/2022-07-06-the-monero-moon-49/19.png)  
*https://revuo-xmr.com/*

Monero упоминается в видео Coin Gecko под названием «Самые популярные монеты 2017 года: где они теперь?» ([Most Popular Coins In 2017: Where Are They Now](https://youtu.be/MC8d9Qgd3gM?t=408)). О Monero говорится на 6:48 минуте. Видео приводится ниже.

{{< youtube id="MC8d9Qgd3gM" autoplay="false" >}}  

Lovera TV опубликовали NOTICIAS sobre MONERO 27/05/2022 al 04/07/2022, видео для испаноговорящих пользователей Monero. Его можно полностью посмотреть [здесь](https://www.youtube.com/watch?v=mKJ9ML2QiHY) или ниже.

{{< youtube id="mKJ9ML2QiHY" autoplay="false" >}}  

### _Мероприятия_

Сегодня в 15:00 UTC Джастин Эхренхофер (Justin Ehrenhofer) примет участие во встрече майнеров на Telegram-канале Crypto Miners. Всю дополнительную информацию можно найти в твите, размещённом ниже.

![20](/img/post/2022-07-06-the-monero-moon-49/20.png)  

Встреча Исследовательской лаборатории Monero будет проведена в среду, 13 июля. Планируется обсуждение таких вопросов, как алгоритмы выбора ложных выходов и анализ аномального объёма транзакций. Соответствующие ссылки и дополнительную информацию о встрече, благодаря Monero Observer, можно найти [здесь](https://monero.observer/monero-research-lab-meeting-13-july-2022/). Встреча лаборатории MRL начнётся в 17:00 UTC на IRC-канале #monero-research-lab. Заглядывайте, если вам интересно, и увидите всё сами в режиме реального времени.

14 июля 2022 г. в Нью-Йорке состоится встреча сообщества Monero. Более подробная информация о событии содержится в [этом посте](https://www.meetup.com/cypherpunk-monero/events/286998154/).

![21](/img/post/2022-07-06-the-monero-moon-49/21.png)  
https://www.meetup.com/cypherpunk-monero/events/286998154/

Опубликовано очередное видео с конференции Monerokon 2022 (перезапись). На видео Конрад Бейчлер (Konrad Baechler) и Марко Пертчерт (Marco Purtschert) рассказывают о попытках деанонимизации участников I2P сети. Видео можно посмотреть здесь.

{{< youtube id="C8qtPl74Uso" autoplay="false" >}}  

### _Биржи и предприниматели_

Вышла предварительная версия децентрализованной биржи Bisq 1.9.3. В новой версии была реализована поддержка подадресов XMR! Более подробная информация содержится в твите ниже.

![22](/img/post/2022-07-06-the-monero-moon-49/22.png)  

Coincards, сервис, осуществляющий продажу подарочных карт за криптовалюту, опубликовал ежемесячный отчёт по используемым криптовалютам (по % и объёму в USD). В июне 2022 г. Monero снова стала самой используемой монетой, составив 51% от всего объёма в США, и второй во всём мире, где объём использования составил 28%! Эти показатели растут в течение последних нескольких месяцев, что свидетельствует о всё большем спросе на Monero.

![23](/img/post/2022-07-06-the-monero-moon-49/23.png)  

Кроме того, теперь Coincards также предлагают купить подарочные карты Steam за XMR!

![24](/img/post/2022-07-06-the-monero-moon-49/24.png)  

Alanzoni опубликовал отчёт по приёму криптовалют предпринимателями начиная с ноября 2019 г. В основу отчёта легли данные, полученные от Accepted Here, регулярно обновляемой базы данных онлайн и офлайн предпринимателей, принимающих к оплате криптовалюту во всём мире. Объём принимаемых к оплате XMR вырос на 314%. Количество предпринимателей, поддерживающих Monero, выросло с 86 до 294, и этот показатель выше, чем в случае с любой другой криптовалютой. Согласно данным Accepted Here, Monero теперь занимает пятую позицию среди самых принимаемых к оплате криптовалют.

![25](/img/post/2022-07-06-the-monero-moon-49/25.png)  

6-7 июля Cake Labs проводили промоакцию, в рамках которой можно было получить 10% дополнительных XMR при обмене любой другой монеты. Если вы проводили обмен с помощью Cake Wallet или Monero.com, то можете потребовать свои 10%. Подробности акции можно найти в этом [посте](https://www.reddit.com/r/Monero/comments/vspeam/promo_10_monero_bonus_when_you_trade_in_cake/).

[MoneroSupplies.com](https://monerosupplies.com/2022/07/04/new-metallic-design-now-available/) предлагает приобрести металлические стикеры! Ознакомиться с товаром можно [здесь](https://monerosupplies.com/2022/07/04/new-metallic-design-now-available/).

![26](/img/post/2022-07-06-the-monero-moon-49/26.png)  
*https://monerosupplies.com/2022/07/04/new-metallic-design-now-available/*

На аукцион были выставлены две редкие металлические монеты Monero 2014 Cryptonic. Увидеть монеты, а также получить ссылки на соответствующие аукционы BitcoinTalk.org можно [здесь](https://www.reddit.com/r/Monero/comments/vq7rx1/2_rare_2014_cryptonic_physical_monero_coins_up/).

![27](/img/post/2022-07-06-the-monero-moon-49/27.png)  
*https://bitcointalk.org/index.php?topic=5404983*

![28](/img/post/2022-07-06-the-monero-moon-49/28.png)  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![29](/img/post/2022-07-06-the-monero-moon-49/29.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![30](/img/post/2022-07-06-the-monero-moon-49/30.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![31](/img/post/2022-07-06-the-monero-moon-49/31.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

Вашему вниманию предлагается еженедельный график XMR/BTC 2016 года, когда 20-недельный индикатор SMA (фиолетовая линия) пересёк 50-недельный SMA (зелёная линия), что стало началом 22-месячного бычьего тренда против BTC. Начиная с конца 2020 г. 20-недельный SMA пересекал 50-недельный лишь в двух случаях, как это и произошло в начале июня 2022. Случится ли это в третий раз?

![32](/img/post/2022-07-06-the-monero-moon-49/32.png)  

Владелец [Moneroj.net](http://moneroj.net/) Morpheus уверен, что XMR находится на довольно серьёзном уровне сопротивления относительно BTC.

![33](/img/post/2022-07-06-the-monero-moon-49/33.png)  

Основатель Cake Wallet Вик Шарма (Vik Sharma) поделился своим взглядом на то, как XMR вела себя недавно в условиях медвежьего рынка.

![34](/img/post/2022-07-06-the-monero-moon-49/34.png)  

Monero является лучшей приватной монетой по рыночной капитализации — рыночная капитализация ZCash составляет менее половины от капитализации Monero.

![35](/img/post/2022-07-06-the-monero-moon-49/35.png)  

Monero стала пятой по популярности монетой среди криптовалют, использующих алгоритм доказательства работы (POW), уступив BTC, ETH, DOGE и LTC, и это несмотря на отсутствие поддержки со стороны ведущих криптовалютных бирж.

![36](/img/post/2022-07-06-the-monero-moon-49/36.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 144 780 XMR
- Общая рыночная капитализация Monero: 2 361 429 904 USD
- Позиция в рейтенге Coinmarketcap: 27
- Цена XMR/USD: 130 USD
- Цена XMR/BTC: 0.00598 BTC
- Цена на LocalMonero.co: 141 USD
- Средний размер комиссии за проведение транзакции: 0.00012 XMR (0.016 USD)
- Хешрейт: 2.518 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![37](/img/post/2022-07-06-the-monero-moon-49/37.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

Переходите по [ссылке](https://www.mixcloud.com/live/xmr_radio/) и слушайте XMR.Radio!

![38](/img/post/2022-07-06-the-monero-moon-49/38.png)  
*https://www.mixcloud.com/live/xmr_radio/*

![39](/img/post/2022-07-06-the-monero-moon-49/39.png)  
*https://twitter.com/afungibleX/status/1544340513406459908*

![40](/img/post/2022-07-06-the-monero-moon-49/40.png)  
*https://twitter.com/LWhatsHisFace/status/1543436367048445954/photo/1*

![41](/img/post/2022-07-06-the-monero-moon-49/41.png)  
*https://www.reddit.com/r/moonero/comments/vqgjnx/monero_summits_digital_painting/*

![42](/img/post/2022-07-06-the-monero-moon-49/42.png)  
*https://boards.4channel.org/biz/thread/50176966*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 49)](https://www.themoneromoon.com/p/the-monero-moon-issue-49)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
