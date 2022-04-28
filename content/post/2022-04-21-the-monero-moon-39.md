---
title: "The Monero Moon (выпуск 39)"
date: "2022-04-21"
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

_The Monero Moon остаётся с вами! Предложение о финансировании еженедельника, размещённое в системе CCS, было одобрено. Спасибо всем тем, кто поддержал нас и внёс пожертвования. The Monero Moon — это на 100% независимое издание. Мы не принимаем никаких спонсорских денег, чтобы и в дальнейшем непредвзято освещать всё происходящее в сообществе Monero. Мы постараемся сделать так, чтобы и впредь наш еженедельник оставался самым исчерпывающим и привлекательным источником новостей Monero. Соберитесь с силами, ведь этот выпуск будет одним из длинных!_

### _Разработка, новые версии и технологии_

Обновление сети Monero (хардфорк) запланировано на 16 июля 2022 года на высоте блока 2 668 888. Это согласованное сообществом Monero обновление, которое позволит повысить уровень приватности и производительность сети Monero, а также потребует, чтобы все пользователи обновили своё программное обеспечение. Новая версия v0.18 Fluorine Fermi будет опубликована за месяц до самого обновления, примерно 16 июня. В рамках обновления будет реализован целый ряд новых свойств, таких как:
- размер кольца увеличится с 11 до 16, что повысит уровень приватности;
- будут реализованы теги просмотра, после чего время синхронизации сократится примерно на 40%;
- в результате обновления протокола до версии Bulletproofs+ размер транзакций сократится примерно на 7% и на столько же повысятся показатели верификации.

Полный список улучшений будет опубликован вместе с новой версией программного обеспечения. Если вы хотите больше узнать о грядущем обновлении сети Monero, ознакомьтесь с этим [постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html), опубликованном на официальном веб-сайте Monero. Вы также можете прочитать [протокол встречи](https://github.com/monero-project/meta/issues/684) разработчиков Monero, состоявшейся 16 апреля, на которой обсуждалось обновление сети.

![01](/img/post/2022-04-21-the-monero-moon-39/01.png)  
_https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html_

Если вы желаете как-то помочь в обновлении сети Monero, достаточно уведомить о нём провайдеров услуг, связанных с кошельками или биржами, в соответствии с этим [контрольным листом обновления](https://github.com/monero-project/meta/issues/690). Это гарантирует, что все стороны своевременно обновят своё программное обеспечение и внесут необходимые изменения.

![02](/img/post/2022-04-21-the-monero-moon-39/02.png)  
_https://github.com/monero-project/meta/issues/690_

Постэмиссия Monero уже не за горами. Она начнётся на высоте блока 2 641 623 приблизительно 8 июня.

![03](/img/post/2022-04-21-the-monero-moon-39/03.png)  

Вы ещё не знаете, что такое постэмиссия и почему она так важна для успешного развития Monero в будущем? Скриншот, размещённый ниже, поможет вам. Также всю нужную информацию можно найти [здесь](https://www.getmonero.org/resources/moneropedia/tail-emission.html) и [здесь](https://localmonero.co/knowledge/monero-tail-emission?language=en).

![04](/img/post/2022-04-21-the-monero-moon-39/04.png)  
_https://www.getmonero.org/resources/moneropedia/tail-emission.html_

![05](/img/post/2022-04-21-the-monero-moon-39/05.png)  

[Аки Маюми](https://www.reddit.com/r/Monero/comments/u7589t/shruum_wallet_alpha_updates_stagenet_apks/) выпустил Shruum, как заявляется, это форк популярного Android-кошелька Monerujo, но без соответствующего раздутия. Shruum подразумевает обязательное использование Tor и использует дополнительные механизмы, обеспечивающие более высокий уровень приватности. Пока что доступна только альфа-версия, поэтому кошелёк рекомендуется только для продвинутых пользователей. Вы сможете узнать больше о Shruum по [этой ссылке](https://www.reddit.com/r/Monero/comments/u7589t/shruum_wallet_alpha_updates_stagenet_apks/).

![06](/img/post/2022-04-21-the-monero-moon-39/06.png)  
_https://www.reddit.com/r/Monero/comments/u7589t/shruum_wallet_alpha_updates_stagenet_apks/_

selsta опубликовал [ежемесячный отчёт](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/279) по результатам своей работы в апреле 2022 в качестве частично занятого разработчика Monero.

![07](/img/post/2022-04-21-the-monero-moon-39/07.png)  
_https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/279_

Представители Haveno, некастодиальной децентрализованной биржи, в основе которой на данный момент лежат протоколы Tor и Monero, опубликовали «Обязательный кодекс поведения контрибьютора» ([Contributor Covenant Code of Conduct](https://github.com/haveno-dex/.github/blob/master/CODE_OF_CONDUCT.md)). Кодекс призван защитить всех участников проекта от всякого рода преследования, независимо от имеющихся между ними отличий.

Monero многократно упоминается в «белой книге», недавно опубликованной учёными Венского университета и Венского технического университета. Документ был назван «Ощутимая приватность пользователей блокчейнов» (User-perceived privacy in blockchain) и представляет собой глубокое исследование приватности, воспринимаемой пользователями блокчейнов на базе UTXO. Авторы выяснили, что Monero является самой популярной приватной монетой. Выдержка и график из белой книги приводятся ниже:

![08](/img/post/2022-04-21-the-monero-moon-39/08.png)  
_https://moneroresearch.info/index.php?action=resource_RESOURCEVIEW_CORE&id=70&browserTabID=_

![09](/img/post/2022-04-21-the-monero-moon-39/09.png)  
_https://moneroresearch.info/index.php?action=resource_RESOURCEVIEW_CORE&id=70&browserTabID=_

Если вы хотите ознакомиться с одной или несколькими работами, посвящёнными или связанными с Monero, посетите [MoneroResearch.info](https://moneroresearch.info/).

![10](/img/post/2022-04-21-the-monero-moon-39/10.png)  
_https://moneroresearch.info/_

Члены сообщества рассматривают возможность предоставления криптовалютными биржами доказательства резерва. «[Протоколы доказательства резерва позволяют криптовалютным биржам доказать собственную платёжеспособность, то есть доказать, что они обладают резервами достаточными для того, чтобы выполнить их обязательства перед клиентами](https://moneroresearch.info/index.php?action=resource_RESOURCEVIEW_CORE&id=35)». Вы можете принять участие в соответствующем обсуждении, перейдя по этой ссылке.

sech1 о назначении премии в размере 3000 USD, которая будет выплачена некоммерческой организацией Нью-Джерси тому, кто создаст генератор персонализированных удобочитаемых адресов (то есть vanity-адресов) Monero. Вы сможете самостоятельно пользоваться таким генератором. Больше информации и соответствующие ссылки можно найти [здесь](https://bitcointalk.org/index.php?topic=5394915.msg59884817).

![11](/img/post/2022-04-21-the-monero-moon-39/11.png)  
_https://bitcointalk.org/index.php?topic=5394915.msg59884817_

Если вам нравится Minecraft, то вам несказанно повезло, поскольку _XxFedexX_ создал первый Minecraft-сервер Monero! Вам достаточно просто перейти по [этой ссылке](https://www.reddit.com/r/Monero/comments/u4d3va/the_first_minecraft_monero_server/).

_imike предлагает использовать удалённый публичный узел в качестве скрытого сервиса Tor, размещённого в высокоскоростной среде, если вы сочтёте это необходимым. Более подробная информация опубликована [здесь](https://bitcointalk.org/index.php?topic=5394915.msg59884817).

[VS41Shamrock](https://www.reddit.com/r/Monero/comments/u53n15/monero_marketing/) предложил создать прозрачную некоммерческую организацию, которая будет заниматься маркетингом Monero. [Здесь](https://www.reddit.com/r/Monero/comments/u53n15/monero_marketing/) вы найдёте соответствующую информацию по теме.

Гарри Хэлпин (Harry Halpin), гендиректор Nym Project, намекнул о возможной интеграции Monero проектом.

![11_](/img/post/2022-04-21-the-monero-moon-39/11_.png)  

Канал [RBM Crypto](https://www.youtube.com/channel/UCuSRfOKOzG7wADtIhqlLZCw) опубликовал видео, в котором рассказывается, как настроить Ledger Nano X с помощью официального GUI-кошелька Monero. Видео можно посмотреть [здесь](https://www.youtube.com/watch?v=kAHcZvFo4_I) или ниже.

{{< youtube id="kAHcZvFo4_I" autoplay="false" >}}  

[The Monero Observer](https://www.monero.observer/) вновь опубликовали отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://www.monero.observer/monero-dev-activity-report-week-15-2022/).

Настоятельно рекомендуем создать и использовать собственный узел или заняться майнингом, так как это способствует защите сети. Также возможен соло-майнинг с помощью официального GUI-кошелька Monero, который можно скачать [здесь](https://www.getmonero.org/downloads/), или, что ещё лучше, пользователи могут заниматься майнингом в пуле, присоединившись к децентрализованному и не требующему разрешений пулу [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html). Если же вы просто хотите создать собственный узел, старый контрибьютор Monero [gingeropolous](https://twitter.com/gingeropolous1) подробно рассказал, как при наличии достаточного терпения сделать это даже с помощью старого лэптопа.

![12](/img/post/2022-04-21-the-monero-moon-39/12.png)  

### _Прочие новости_

18 апреля проект Monero отпраздновал свой восьмой день рождения! К этой дате [Wataru_Watanabe](https://www.reddit.com/r/Monero/comments/u66eqq/8_years_of_monero/) опубликовал эту фантастическую графику!

![13](/img/post/2022-04-21-the-monero-moon-39/13.png)  
_https://www.reddit.com/r/Monero/comments/u66eqq/8_years_of_monero/_

reemuru разместил на официальном веб-сайте Monero замечательный пост под названием «Чем запомнится этот год для Monero — 2022» ([This Year in Monero – 2022](https://www.getmonero.org/2022/04/18/this-year-in-monero.html)), свидетельствующий о непрерывном росте Monero. Среди прочего в посте отмечается следующее:
- за прошедший год частота проведения транзакций в блокчейне выросла на 154%;
- в прошедшем году размер блокчейна увеличивался на 144% быстрее;
- показатель инфляции снизился на 34%, и проект стабильно приближается к точке начала [постэмиссии](https://localmonero.co/knowledge/monero-tail-emission), когда размер вознаграждения за добычу блока станет равен 0,6 XMR;
- средний размер комиссии за проведение транзакции снизился на 48%;
- хешрейт сети повысился на 53%;
- количество подписчиков @monero в Twitter и  r/monero на Reddit вырослор более чем на 20% в обоих случаях.

![14](/img/post/2022-04-21-the-monero-moon-39/14.png)  
_Количество подписчиков reddit.com/r/monero_

![15](/img/post/2022-04-21-the-monero-moon-39/15.png)  

Члены сообщества Monero также воспользовались днём рождения Monero, чтобы принятие участие в Monerun, мероприятия, в ходе которого пользователи выводят свои XMR с бирж, чтобы повысить уровень приватности криптовалюты и ограничить запасы XMR у таких бирж, а также выявить возможные случаи частичного резервирования некоторыми недобросовестными биржами. В Telegram даже была создана группа, [состоящая из членов сообщества Monero](https://t.me/moneroexchangerun), поддерживающих это движение. Эти представители сообщества [утверждают](https://www.reddit.com/r/xmrtrader/comments/tzn6hj/xmr_withdrawals_disabled/), что подобные недобросовестные биржи периодически переводят кошельки XMR или функцию вывода средств в «режим обслуживания», что свидетельствует о том, что биржи на самом деле не имеют того количества XMR, что заявляется ими. И не забывайте о следующем: «не ваши ключи — не ваши монеты». То есть если вы не храните монеты у себя, то, по сути, вы и не владеете ими.

[bawdyanarchist опубликовал великолепный набор часто задаваемых вопросов по Monerun](https://www.reddit.com/r/Monero/comments/u57qky/the_monerun_faq_responses_ideas/). Рекомендуем ознакомиться с ним, даже если вы не имеете и малейшего понятия о том, что это такое.

![16](/img/post/2022-04-21-the-monero-moon-39/16.png)  
_Автор: [BluWorm](https://www.reddit.com/user/BluWorm/) - https://www.reddit.com/r/Monero/comments/u4u3o2/to_new_members_and_those_at_the_back/_

Стихийное движение Monerun даже привлекло внимание многих организаций.

Coindesk опубликовали статью, посвящённую обновлению сети Monero и Monerun, под названием «Ориентированный на обеспечение приватности проект Monero планирует хардфорк на июль. Цена XMR отыгрывает 11% после проведения Monerun» ([Privacy Focused Monero Plans Hard Fork in July; XMR Surges 11% on ‘Monerun’](https://www.coindesk.com/markets/2022/04/19/privacy-focused-monero-plans-hard-fork-in-july-xmr-surges-11-on-monerun/)).

![17](/img/post/2022-04-21-the-monero-moon-39/17.png)  
_https://www.coindesk.com/markets/2022/04/19/privacy-focused-monero-plans-hard-fork-in-july-xmr-surges-11-on-monerun/_

Decrypt опубликовали статью, посвящённую Monerun, под заголовком «Monero совершает праведный набег на биржи, чтобы проверить их резервы» ([Monero Faithful Coordinate ‘Bank Run’ to Test Exchanges’ Reserves](https://decrypt.co/98023/monero-faithful-threaten-bank-run-on-centralized-exchanges)).

![18](/img/post/2022-04-21-the-monero-moon-39/18.png)  
_https://decrypt.co/98023/monero-faithful-threaten-bank-run-on-centralized-exchanges_

Bloomberg также осветили мероприятие Monerun и последовавший рост цены криптовалюты в статье «Цена альткоина Monero растёт на фоне вывода владельцами этой криптовалюты своих активов с бирж» (Altcoin Monero Surges as Owners Set Withdrawal From Exchanges).

![19](/img/post/2022-04-21-the-monero-moon-39/19.png)  
_https://www.bloomberg.com/news/articles/2022-04-18/altcoin-monero-surges-as-owners-set-withdrawal-from-exchanges_

Vice опубликовали статью, посвящённую Monerun, под названием «Владельцы Monero массово выводят свои активы с бирж, чтобы проверить их» ([Monero Owners Are Staging a Crypto Bank Run to Test Exchanges](https://www.vice.com/en/article/qjb9n3/monero-owners-mass-withdrawal-monerun)).

![20](/img/post/2022-04-21-the-monero-moon-39/20.png)  
_https://www.vice.com/en/article/qjb9n3/monero-owners-mass-withdrawal-monerun_

Maxbit тоже опубликовали отличную и подробную статью,  повествующую о Monerun, под заголовком «Блицкриг сообщества Monero на централизованные биржи в рамках грядущего Monerun» ([Monero community set to blitz CEXs in coming ‘Monerun’](https://maxbit.cc/monero-community-set-to-blitz-cexs-in-coming-monerun/))

![21](/img/post/2022-04-21-the-monero-moon-39/21.png)  
_https://maxbit.cc/monero-community-set-to-blitz-cexs-in-coming-monerun/_

InvestorPlace опубликовали статью «Цена XMR подскочила на фоне координированного массового вывода Monero быками» ([XMR Crypto Prices Spike as Monero Bulls Coordinate Mass Withdrawals](https://investorplace.com/2022/04/xmr-crypto-prices-spike-as-monero-bulls-coordinate-mass-withdrawals/)).

![22](/img/post/2022-04-21-the-monero-moon-39/22.png)  
_https://investorplace.com/2022/04/xmr-crypto-prices-spike-as-monero-bulls-coordinate-mass-withdrawals/_

[Gate.io](https://www.youtube.com/channel/UCChFMpMMqduaUuGGCPIn9xw) вышли в прямой эфир YouTube с видео, в котором обсудили обновление сети Monero и мероприятие Monerun. Видео можно посмотреть ниже.

{{< youtube id="abqKC36f-as" autoplay="false" >}}  

Bitcoin Magazine опубликовали статью «Ориентированный на обеспечение приватности проект Monero в июле планирует произвести хардфорк. Планируется изменение кольцевой подписи и усовершенствование протокола Bulletproof» ([Privacy-Centric Monero Plans for July Hard Fork, Plans Include Ring Signature, Bulletproof Upgrade](https://news.bitcoin.com/privacy-centric-monero-plans-for-july-hard-fork-plans-include-ring-signature-bulletproof-upgrade/)).

![23](/img/post/2022-04-21-the-monero-moon-39/23.png)  
_https://news.bitcoin.com/privacy-centric-monero-plans-for-july-hard-fork-plans-include-ring-signature-bulletproof-upgrade/_

Вышел девятый номер [The Monero Standard](https://localmonero.co/the-monero-standard/weekly/9) с очередной порцией еженедельных новостей Monero.

[Monero Talk](https://www.youtube.com/channel/UC3Hx81QYLoEQkm3vyl4N4eQ) отпраздновали восьмой день рождения Monero в прямом эфире. Также в очередном эфире говорилось о Monerorun. Получившееся видео можно посмотреть ниже!

{{< youtube id="wY_BZczHZ4Y" autoplay="false" >}}  

Даг из Monero Talk также предпринял публичную попытку продемонстрировать, насколько просто убедить пользователей или предпринимателей начать принимать XMR в качестве оплаты. Это некоторым образом напомнило попытку Роджера Вера на заре существования Bitcoin.

![24](/img/post/2022-04-21-the-monero-moon-39/24.png)  

[The Open Economy Initiative](https://www.youtube.com/channel/UC9kj55zHAw8PUlkO31-1j7Q) разместили новое видео, в котором обсудили недавнюю конференцию Monerotopia и прочие события Monero. Видео можно посмотреть ниже.

{{< youtube id="zNfZy1KtzdQ" autoplay="false" >}}  

Как [сообщается](https://www.reddit.com/r/Monero/comments/u3ngp0/edward_snowden_speaking_at_station_f_for_the/), Эдвард Сноуден в своём недавнем выступлении по случаю запуска Nym назвал Monero лучшей приватной альтернативой Bitcoin.

![25](/img/post/2022-04-21-the-monero-moon-39/25.jpeg)  
_https://www.reddit.com/r/Monero/comments/u3ngp0/edward_snowden_speaking_at_station_f_for_the/_

Tornado Cash, популярный сервис, обеспечивающий приватность Ethereum, объявил об использовании оракула Chainalysis с целью блокировки попавших под санкции транзакций.

![26](/img/post/2022-04-21-the-monero-moon-39/26.png)  

Cipher Trace опубликовали твит, согласно которому группы злоумышленников, занимающихся вымогательством, всё чаще требуют выплаты в Monero. В твите также говорится, что Monero постепенно смещает Bitcoin с места самой популярной рыночной валюты в даркнете.

![27](/img/post/2022-04-21-the-monero-moon-39/27.png)  

[Cointelegraph также коснулись этой истории](https://cointelegraph.com/news/monero-crypto-of-choice-as-ransomware-double-extortion-attacks-increase-500), разъяснив, что «в течение прошедшего года наблюдался рост вымогательства с использованием криптовалюты Monero (XMR), которую злоумышленники стали предпочитать Bitcoin ([BTC](https://cointelegraph.com/bitcoin-price)) в 10-20% случаев. По крайней мере, в 22 случаях вымогательства (из неполного списка, включающего в себя 50 случаев) принимались выплаты только в Monero ([XMR](https://cointelegraph.com/xmr-price-index)), и, по крайней мере, в семи из них вымогатели требовали как BTC, так и XMR».

![28](/img/post/2022-04-21-the-monero-moon-39/28.png)  
_https://cointelegraph.com/news/monero-crypto-of-choice-as-ransomware-double-extortion-attacks-increase-500_

### _Мероприятия_

Встреча Monero Space запланирована на субботу, 23 апреля 2022 (17:00 UTC) на IRC-канале #monero-space. К участию приглашаются все желающие, даже если вы захотите просто поглазеть.

![29](/img/post/2022-04-21-the-monero-moon-39/29.png)  
_https://github.com/monero-project/meta/issues/692_

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет [Arroz Studios](https://arrozestudios.pt/). Если вы же хотите принять участие, на сайте принимаются предложения по проведению презентаций и семинаров. MoneroKon станет фестивалем всего, связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Билеты на MoneroKon теперь можно приобрести [здесь](https://monerokon.com/products/monerokon2022), на веб-сайте MoneroKon.

Очередная плановая встреча по проведению MoneroKon 2022 состоится в субботу, 23 апреля 2022 года в 18:00 UTC на IRC-канале #monero-events.

![30](/img/post/2022-04-21-the-monero-moon-39/30.png)  
_https://monerokon.com/_

В честь дня рождения Monero [spesmonerujo](https://moneropost.com/) разыгрывает один ноут Carbon Chameleon. Всё, что нужно сделать — пожертвовать 0,001 XMR в общий фонд и опубликовать хеш вашей транзакции в твите, как это показано ниже.

![31](/img/post/2022-04-21-the-monero-moon-39/31.png)  

### _Биржи и предприниматели_

Ориентированный на обеспечение приватности обменный сервис [Majestic Bank](https://majesticbank.sc/) на практике поддержал недавнее мероприятие Monerun. Все комиссии, полученные сервисом, 18 апреля были пожертвованы проекту Monero. Всего было собрано 8000 USD, которые затем были переданы сообществу Monerop для реализации различных инициатив и проектов. Больше информации можно найти по [этой ссылке](https://www.reddit.com/r/Monero/comments/u75ehm/it_was_majestic_day_8000_usd_collected_for/). Majestic Bank также предлагает воспользоваться [Tor-версией своего веб-сайта](https://majestictfvnfjgo5hqvmuzynak4kjl5tjs3j5zdabawe6n2aaebldad.onion/).

![32](/img/post/2022-04-21-the-monero-moon-39/32.jpeg)  
_https://majesticbank.sc/_

Хотите выиграть несколько XMR? Заходите на [MoneroPot.org](https://moneropot.org/), отправьте несколько XMR посредством этого сервиса и примите участие в очередном розыгрыше.

![33](/img/post/2022-04-21-the-monero-moon-39/33.png)  
_https://moneropot.org/_

Целый ряд криптовалютных бирж, предлагающих возможность обмена XMR на другие валюты, испытал сложности с выводом, в результате чего было решено провести мероприятие Monerun, в ходе которого также наблюдались схожие проблемы. Членами сообщества [было отмечено](https://www.reddit.com/r/Monero/comments/u5wxrt/network_busy_please_try_again_laterbinance/), что биржи Binance, Huobi и Poloniex в определённый момент ограничили возможность вывода. Помимо этого, статистический криптовалютный веб-сайт Coingecko даже получил запросы об исключении из публикуемых данных некоторых бирж при подсчёте показателей XMR.

Поставщики стикеров Monero MoneroSupplies.com предлагают скидку при оформлении международных заказов. Более подробную информацию можно найти [здесь](https://monerosupplies.com/2022/04/19/cheaper-international-shipping-for-small-orders/).

CAN-USA разрабатывают MoneroPost.com, веб-сайт, целью которого станет обеспечение возможности приобретения пользователями почтовых наклеек и транспортных этикеток USPS, UPS, Canada Post, FedEx, DHL и Deutsche Post за Monero. С подробностями можно ознакомиться [здесь](https://moneropost.com/).

![34](/img/post/2022-04-21-the-monero-moon-39/34.png)  
_https://moneropost.com/_

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но, если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![35](/img/post/2022-04-21-the-monero-moon-39/35.png)  

selsta опубликовал предложение, предложив свои услуги в качестве разработчика Monero (частичная занятость). Предложение можно найти [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/312).

Moneroist также разместил предложение по разработке Patronero, открытого проекта, который позволит делать пожертвования с помощью майнинга. Более подробную информацию по данному предложению можно найти по этой ссылке.

CryptoGrampy опубликовал в системе CCS предложение по созданию браузерного, эфемерного, бессерверного веб-приложения Point of Sale для Monero. С предложением можно ознакомиться [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/307).

willk разместил в CCS предложение под названием «Решения Monero для работы со множеством сцен» ([Multi-scene monero solutions](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/311)).

Дональд А. Ильязи (Donald A. Iljazi) внёс предложение по переводу приложений, веб-сайтов и прочих материалов на греческий язык. Соответствующее предложение размещено [здесь](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/296).

[Предложение](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/294) The Monero Moon перемещено в раздел «Требуется финансирование»! Если вам нравится читать The Monero Moon, пожалуйста, поддержите нас.

Предложение [mj](https://repo.getmonero.org/mj) о создании нового проекта под названием [SolOptXMR](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/299) (Оптимальный солнечный майнинг XMR) всё ещё ожидает финансирования.

Предложение savandra по созданию [новых анимированных видео Monero](https://ccs.getmonero.org/proposals/savandra-videos-for-monero.html) в настоящее время открыто для финансирования.

### _Торговля и биржевые спекуляции_

Спустя 4 года нисходящего тренда Monero относительно Bitcoin XMR наконец-то испытала подъём. Это редкий и беспрецедентный случай для любой криптовалюты, когда ей удаётся выйти из затяжного падения в паре с BTC, и, насколько мне известно, ранее такого не происходило. Последний раз, когда такое случалось (также в паре XMR/BTC) был зафиксирован в феврале 2016 перед 2600% ралли относительно Bitcoin.

![36](/img/post/2022-04-21-the-monero-moon-39/36.png)  

Авторитетный пользователь Twitter под ником Don Yakka даёт собственный прогноз в отношении пары XMR/USD.

![37](/img/post/2022-04-21-the-monero-moon-39/37.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 110 450 XMR
- Общая рыночная капитализация Monero: 5 003 708 931 USD
- Позиция в рейтенге Coinmarketcap: 33
- Цена XMR/USD: 276 USD
- Цена XMR/BTC: 0,00660 BTC
- Цена на LocalMonero.co: 258 USD
- Средний размер комиссии за проведение транзакции: 0.00014 XMR ($0.03)
- Хешрейт: 3.063 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![38](/img/post/2022-04-21-the-monero-moon-39/38.png)  
_https://minexmr.com/pools.html_

### _Для развлечения_

![39](/img/post/2022-04-21-the-monero-moon-39/39.png)  
_https://monero.graphics/_

![40](/img/post/2022-04-21-the-monero-moon-39/40.png)  
_https://www.reddit.com/r/Monero/comments/u6clri/doing_my_part_for_monerun/_

![41](/img/post/2022-04-21-the-monero-moon-39/41.jpeg)  
_https://www.reddit.com/r/Monero/comments/u7ebgo/monero_pizza/_

![42](/img/post/2022-04-21-the-monero-moon-39/42.jpeg)  
_https://twitter.com/MoneroArchive/status/1516744045372100609/photo/1_

![43](/img/post/2022-04-21-the-monero-moon-39/43.jpeg)  
_https://www.reddit.com/r/moonero/comments/u1x5es/use_monero_sidarta0_mixed_medium/_

![44](/img/post/2022-04-21-the-monero-moon-39/44.png)  
_https://www.reddit.com/r/CryptoMarkets/comments/u72eqx/jimmy_song_tells_people_not_to_use_monero_for/_

![45](/img/post/2022-04-21-the-monero-moon-39/45.png)  
_https://boards.4channel.org/biz/thread/48117919_

[Инвестору Monero удаётся спастись в кораблекрушении!](https://www.crypticinvestor.com/2022/04/monero-investor-barely-escapes-with-his.html)

Наконец, рекомендуем посетить [Artistic Saturday от Monero Observer](https://www.monero.observer/monero-observer-artistic-saturday-week-15-2022/). Здесь вы найдёте крутую подборку рисунков и прочих произведений на тему Monero!

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 39)](https://www.themoneromoon.com/p/the-monero-moon-issue-39)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
