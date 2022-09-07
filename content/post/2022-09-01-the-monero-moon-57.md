---
title: "The Monero Moon (выпуск 57)"
date: "2022-09-01"
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

_Внимание! В сентябре The Monero Moon выходить не будет. Мы надеемся вернуться 6 октября 2022. В это время новости Monero можно будет найти в следующих источниках_:
- [Monero Observer](https://monero.observer/)
- [The Monero Standard](https://localmonero.co/the-monero-standard?language=en)
- [Revuo Monero](https://revuo-xmr.com/)

_Помимо этого, запрос в системе CCS на финансирование дайджеста The Monero Moon в течение последующих 18 месяцев по-прежнему открыт. Я был бы крайне признателен, если бы вы оставили свои комментарии, перейдя по этой ссылке. В зависимости от результата финансирования по указанному запросу, существует вероятность, что дайджест The Monero Moon выходить перестанет. Но, независимо от результата, мне было очень приятно внести свой вклад в дело сообщества Monero, так что предлагаю поднять бокал в честь разработчиков Monero!_

### _Разработка, новые версии и технологии_

[ACK-J](https://github.com/ACK-J) поделился новостями о ходе своей работы по оценке поверхности атаки кольцевых подписей с точки зрения машинного и глубокого обучения. В рамках аудита безопасности и устойчивости кольцевых подписей Monero к атакам с применением искусственного интеллекта предлагается три разных модели, лучшая из которых позволяет достигнуть 13,3% точности при нахождении действительного выхода при проведении транзакций в основной сети, что всего на 4,3% лучше, чем при случайном угадывании. Более подробную информацию о работе ACK-J можно найти [здесь](https://github.com/MAGICGrants/Monero-Fund/issues/15), окончательный вариант отчёта опубликован по [этой ссылке](https://github.com/ACK-J/Monero-Dataset-Pipeline/blob/main/Lord_of_the_Rings__An_Empirical_Analysis_of_Monero_s_Ring_Signature_Resilience_to_Artificially_Intelligent_Attacks.pdf).

![01](/img/post/2022-09-01-the-monero-moon-57/01.png)  
*https://github.com/ACK-J/Monero-Dataset-Pipeline/blob/main/Lord_of_the_Rings__An_Empirical_Analysis_of_Monero_s_Ring_Signature_Resilience_to_Artificially_Intelligent_Attacks.pdf*

Сообщаем о выходе новой версии [Monero-Bash v1.8.3](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.8.3). Monero-bash — это написанная на Bash оболочка/менеджер Linux для monerod, monero-wallet-cli, XMRig и P2Pool. Согласно [видео](https://www.reddit.com/r/Monero/comments/u0s8z5/monerobash_v100_released/), monero-bash можно использовать для скачивания, настройки и майнинга посредством P2Pool. И на всё это потребуется не более двух минут. И не забывайте, [monero-bash v2.0.0 уже в разработке](https://github.com/hinto-janaiyo/monero-bash/releases/tag/v1.7.0), так что скоро версии v1.x.x станут несовместимыми.

![02](/img/post/2022-09-01-the-monero-moon-57/02.png)  
*https://github.com/hinto-janaiyo/monero-bash*

Вышла версия v13.2.0 MMGen, онлайн/офлайн кошелька Monero с поддержкой командной строки. Как сказано на странице MMGen в GitHub, «MMGen — это кошелёк и средство для «холодного» хранения Bitcoin (и некоторых альткоинов), реализованное в виде набора простых скриптов Python. Скрипты работают в тандеме с базовым демоном Bitcoin или альткоина как в онлайн, так и в офлайн режиме, что обеспечивает возможность надёжного и безопасного хранения, отслеживания, отправки и получения вашей криптовалюты». Более подробную [информацию](https://www.reddit.com/r/Monero/comments/x2dh8p/version_1320_of_the_mmgen_onlineoffline/) можно найти на странице MMGen на [GitHub](https://github.com/mmgen/mmgen) или [GitLab](https://gitlab.com/MMGen/mmgen).

![03](/img/post/2022-09-01-the-monero-moon-57/03.png)  
*https://github.com/mmgen/mmgen*

После недавних проблем с обновлением программного обеспечения после хардфорка Monero сервисы кошелька MyMonero снова работают на всех их платформах.

![04](/img/post/2022-09-01-the-monero-moon-57/04.png)  

Также сообщается о выходе версии v2.20.2 кошелька Edge, который после обновления сети полностью поддерживает Monero.

![05](/img/post/2022-09-01-the-monero-moon-57/05.png)  

Основатель Whonix Патрик Шлейцер (Patrick Schleizer) обновил GUI и CLI кошельки до версии 0.18.1.0 в целях обеспечения совместимости после обновления сети Monero в прошлом месяце.

![06](/img/post/2022-09-01-the-monero-moon-57/06.png)  
*https://forums.whonix.org/t/monero-integration-in-whonix/5949/68*

[SChernykh](https://github.com/SChernykh) опубликовал новую версию [P2Pool v2.3](https://github.com/SChernykh/p2pool/releases/tag/v2.3). Обновлённая версия содержит самые различные усовершенствования. Так, например, был улучшен процесс синхронизации при запуске. Помимо этого, были исправлены некоторые незначительные ошибки. Из [этого поста](https://github.com/SChernykh/p2pool/releases/tag/v2.3) можно узнать, как произвести обновление, а также получить дополнительную информацию.

![07](/img/post/2022-09-01-the-monero-moon-57/07.png)  
*https://github.com/SChernykh/p2pool/releases/tag/v2.3*

29 августа P2Pool отпраздновал свой первый день рождения! Именно в этот день с помощью P2Pool на высоте 2 437 679 был вычислен первый блок. sech1 поделился [статистикой работы](https://www.reddit.com/r/Monero/comments/x0jdb3/p2pools_first_anniversary_is_today/) P2Pool за первый год: майнерами было добавлено 12 118 блоков, за что они получили более 8365 XMR, а количество отдельных выплат составило 943 595. На данный момент P2Pool является четвёртым по величине пулом.

![08](/img/post/2022-09-01-the-monero-moon-57/08.png)  
*https://www.reddit.com/r/Monero/comments/x0jdb3/p2pools_first_anniversary_is_today/*

Hathzed опубликовал краткое руководство по быстрой настройке узла Monero и P2Pool! С руководством можно ознакомиться [здесь](https://twitter.com/hathzed/status/1563501793044152325).

![09](/img/post/2022-09-01-the-monero-moon-57/09.png)  

Всем рекомендуется создать и поддерживать собственный узел — это способствует повышению уровня безопасности сети Monero. Также можно заняться соло-майнингом с помощью официального GUI-кошелька Monero, который можно скачать [здесь](https://www.getmonero.org/downloads/), или же воспользовавшись децентрализованным и не требующим каких-либо разрешений пулом [P2Pool](https://www.getmonero.org/2021/10/05/p2pool-released.html). Официальный веб-сайт Monero [getmonero.org](https://www.getmonero.org/get-started/mining/) или сайт [sethforprivacy.com](https://sethforprivacy.com/guides/) помогут вам создать и запустить узел или заняться майнингом.

![10](/img/post/2022-09-01-the-monero-moon-57/10.png)  

После недавнего закрытия майнинг-пула MineXMR хешрейт Monero стал более децентрализованным, чем когда-либо. Хешрейт P2Pool продолжает расти. За прошлую неделю он вырос с 164,30 Mh/s до 178,28 Mh/s.

![11](/img/post/2022-09-01-the-monero-moon-57/11.png)  
*https://minexmr.com/pools.html*

[duggavo](https://github.com/duggavo) создал [MoneroBlock](https://github.com/duggavo/MoneroBlock/), не требующий доверенных настроек блокчейн-эксплорер для платёжной сети Monero. Блокчейн-эксплореры можно использовать в качестве инструмента для деанонимизации транзакций, поэтому следует быть предельно внимательными при выборе эксплорера. Список доступных блокчейн-эксплореров Monero как для луковой сети, так и клирнета можно найти [здесь](https://github.com/moneroexamples/onion-monero-blockchain-explorer).

![12](/img/post/2022-09-01-the-monero-moon-57/12.png)  
*https://github.com/duggavo/MoneroBlock/*

[Monero Observer](https://www.monero.observer) опубликовали подробный отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-34-2022/).

![13](/img/post/2022-09-01-the-monero-moon-57/13.png)  
*https://monero.observer/monero-dev-activity-report-week-34-2022/*

### _Прочие новости_

[Seth For Privacy](https://twitter.com/sethforprivacy) принял участие в сессии Twitter Spaces, проводимой CoinDesk, под названием «[Жизнь после Tornado Cash, или как защитить приватность вашей финансовой информации](https://twitter.com/i/spaces/1vAxRAaopLRJl)». Seth выступил на шестнадцатой минуте. Очень рекомендуем к прослушиванию.

![14](/img/post/2022-09-01-the-monero-moon-57/14.png)  
*https://twitter.com/i/spaces/1vAxRAaopLRJl*

[Monero Talk](https://www.youtube.com/watch?v=EvMPzC7RFsU) взяли интервью у Питера Ван Валькенбурга ([Peter Van Valkenburgh](https://twitter.com/valkenburgh/)), директора по исследованиям из CoinCenter. Даг и Питер обсудили историю юридических проблем, связанных с криптовалютой, Управлением по контролю за иностранными активами (OFAC), а также текущее состояние норм AML и то, как случай с Tornado Cash повлиял на экосистему Monero. Кроме того, участники беседы сравнили Monero, Zcash и Bitcoin в контексте регулятивных норм, а также рассмотрели целую массу других вопросов. Интервью можно посмотреть по [этой ссылке](https://www.youtube.com/watch?v=EvMPzC7RFsU).

{{< youtube id="EvMPzC7RFsU" autoplay="false" >}}  

Также Monero Talk опубликовали восьмидесятый эпизод [Monerotopia](https://www.youtube.com/watch?v=jYZkzrxMVi4). В этом эпизоде рассказывается об участии команды Monero Talk во встрече под названием «Протест Monero ради сохранения приватности» (Monero Privacy Protest), прошедшей в Нью-Йорке, приводится отчёт по цене от [aFungible](https://twitter.com/afungibleX), а также интервью с ведущим разработчиком Thorchain Чадом Бэррафордом (Chad Barraford). Полностью эпизод можно найти [здесь](https://www.youtube.com/watch?v=jYZkzrxMVi4).

{{< youtube id="jYZkzrxMVi4" autoplay="false" >}}  

Согласно результатам исследования, проведённого Check Point Software Technologies, с помощью турецкого вредоносного программного обеспечения под названием Nitrokod, которым были заражены машины в 11 странах, злоумышленники занимались майнингом XMR с помощью машин пользователей. Более подробно об этом можно прочитать [здесь](https://research.checkpoint.com/2022/check-point-research-detects-crypto-miner-malware-disguised-as-google-translate-desktop-and-other-legitimate-applications/), на веб-сайте Check Point, а новостную статью, посвящённую указанному программному обеспечению, можно найти по [этой ссылке](https://cryptonews.net/news/security/11443923/).

![15](/img/post/2022-09-01-the-monero-moon-57/15.png)  
*https://research.checkpoint.com/2022/check-point-research-detects-crypto-miner-malware-disguised-as-google-translate-desktop-and-other-legitimate-applications/*

Вышел 134-й выпуск [Revuo Monero](https://revuo-xmr.com). Переходите по ссылке, чтобы получить еженедельную дозу новостей Monero.

Как сообщает Defiant, на этой неделе Hetzner, второй по величине хостинг-провайдер Ethereum, завил, что майнеры не могут использовать его сервера для поддержки блокчейна, равно как и любой другой деятельности, связанной с криптовалютой.

![16](/img/post/2022-09-01-the-monero-moon-57/16.png)  
*https://www.thedefiant.io/data-giant-shocks-ethereum-with-ban-on-mining*

### _Встречи и мероприятия_

Сегодня в 16:30 в Кейптауне, Южная Африка, в ресторане La Parada пройдёт встреча сообщества Monero. Приглашаем всех желающих присоединиться к обсуждению недавнего обновления сети Monero. Более подробная информация о встрече размещена [здесь](https://www.meetup.com/cape-town-privacy-meetup-group/events/287980729/).

![17](/img/post/2022-09-01-the-monero-moon-57/17.png)  
*https://www.meetup.com/cape-town-privacy-meetup-group/events/287980729/*

Встреча Исследовательской лаборатории Monero (MRL) будет проведена в среду, 7 сентября, в 17:00 UTC. Соответствующие ссылки и дополнительную информацию о встрече, благодаря Monero Observer, можно найти здесь. Встреча лаборатории MRL пройдёт на IRC-канале #monero-research-lab. Заглядывайте и увидите всё сами в режиме реального времени.

На Хэллоуин, 31 октября, в 18:00 в Нью-Йорке в Вашингтон-Сквер-парк пройдёт протест в поддержку приватности, организованный командой Monero Talk. Маски для участников предоставляются бесплатно! Все подробности ищите на веб-сайте [Monerotopia](https://monerotopia.com).

![18](/img/post/2022-09-01-the-monero-moon-57/18.png)  
*https://monerotopia.com/*

### _Биржи и предприниматели_

[AllArk](https://allark.io) теперь поддерживает подарочные карты Airbnb. Сервис доступен для жителей Европы, Великобритании и Австралии. AllArk не требует соблюдения правила KYC и продаёт предоплаченные карты Visa и подарочные карты за XMR. Сервис чем-то похож на Cake Pay, а на их сайт можно перейти по [этой ссылке](https://allark.io/).

![19](/img/post/2022-09-01-the-monero-moon-57/19.png)  
*https://allark.io/*

Веб-сайт Monero.com претерпел обновления: была добавлена новая синяя тема, а также усовершенствован блокчейн-эксплорер. Теперь, благодаря новой цветовой теме и рекламному баннеру, сайт отличается от официального веб-сайта GetMonero.org, что позволяет избежать путаницы. Более подробную информацию по обновлению можно найти [здесь](https://www.reddit.com/r/Monero/comments/x0t27o/monerocom_website_updated_with_new_blue_color/).

![20](/img/post/2022-09-01-the-monero-moon-57/20.png)  
*https://monero.com/*

Cake Labs опубликовали на YouTube видео, в котором показано, как пользоваться Cake Pay для онлайн платежей, а также как пользоваться подарочными картами с кошельками Cake Wallet и Monero.com. Обращаем ваше внимание, что Cake Pay пока работает только на территории США. Видео можно посмотреть [здесь](https://www.youtube.com/watch?v=2Ur7FExvTPM).

{{< youtube id="2Ur7FExvTPM" autoplay="false" >}}  

[Cryptwerk](https://cryptwerk.com/pay-with/xmr/) создал директорию, содержащую ссылки более чем на 1200 предпринимателей, принимающих к оплате XMR по всему миру. Если вы хотите оплачивать товары или сервисы с помощью Monero, заходите на их веб-сайт.

![21](/img/post/2022-09-01-the-monero-moon-57/21.png)  
*https://cryptwerk.com/pay-with/xmr/*

[Bitcoinist](https://bitcoinist.com/interview-with-mike-changenow-was-the-only-platform-to-support-monero-during-fork/) опубликовал интервью с Майком из ChangeNow, мгновенной биржи, поддерживающей XMR. Статью можно найти по [этой ссылке](https://bitcoinist.com/interview-with-mike-changenow-was-the-only-platform-to-support-monero-during-fork/).

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![22](/img/post/2022-09-01-the-monero-moon-57/22.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![23](/img/post/2022-09-01-the-monero-moon-57/23.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования или недавно профинансированные:**_

Фонд MAGIC Monero собирает средства на финансирование работы noot по реализации атомных свопов ETH-XMR. Соответствующую страницу GoFundMe можно найти по [этой ссылке](https://www.gofundme.com/f/noot-ethxmr-atomic-swap-development-4-months). [Здесь](https://magicgrants.budibase.app/app/magic-monero-fund-donations) вы также можете сделать пожертвование напрямую в криптовалюте или с помощью кредитной/дебетовой карты.

![24](/img/post/2022-09-01-the-monero-moon-57/24.png)  
*https://www.gofundme.com/f/noot-ethxmr-atomic-swap-development-4-months*

![25](/img/post/2022-09-01-the-monero-moon-57/25.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

Untraceable откорректировал возможный фрактальный паттерн пары XMR/BTC.

![26](/img/post/2022-09-01-the-monero-moon-57/26.png)  

Несмотря на то, что обширная часть рынка пребывает в медвежьем тренде, пара XMR/BTC впервые с апреля 2019 демонстрирует простую скользящую среднюю.

![27](/img/post/2022-09-01-the-monero-moon-57/27.png)  

Согласно техническому анализу Tradingview, пара XMR/BTC может заинтересовать быков.

![28](/img/post/2022-09-01-the-monero-moon-57/28.png)  

Зелёное в море красного.

![29](/img/post/2022-09-01-the-monero-moon-57/29.png)  

Модель соотношения запасов к потоку Monero довольно низка и демонстрирует сильное отклонение от цены S2F.

![30](/img/post/2022-09-01-the-monero-moon-57/30.png)  

_**Показатели**_
- Общее количество Monero в обращении: 18 168 467 XMR
- Общая рыночная капитализация Monero: 2 774 663 183 USD
- Позиция в рейтенге Coinmarketcap: 27 (27 на прошлой неделе)
- Цена XMR/USD: 152 USD
- Цена XMR/BTC: 0.007599 BTC
- [Цена на LocalMonero.co](https://localmonero.co/statistics?language=en): 160 USD
- Средний размер комиссии за проведение транзакции: 0.000031 XMR (0.047 USD)
- Хешрейт: 2.517 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![31](/img/post/2022-09-01-the-monero-moon-57/31.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![32](/img/post/2022-09-01-the-monero-moon-57/32.png)  
*https://www.reddit.com/r/moonero/comments/wznim2/collect_coins/*

![33](/img/post/2022-09-01-the-monero-moon-57/33.png)  
*https://i.4cdn.org/biz/1646797688491.png*

![34](/img/post/2022-09-01-the-monero-moon-57/34.png)  
*https://www.reddit.com/r/moonero/comments/wv6tog/another_day_in_the_life_of_a_bitcoin_maxi/*

![35](/img/post/2022-09-01-the-monero-moon-57/35.png)  
*https://www.reddit.com/r/moonero/comments/wqz807/there_is_no_fate_but_what_we_make_for_ourselves/*  

![36](/img/post/2022-09-01-the-monero-moon-57/36.png)  
*https://peakd.com/meme/@stevescoins/monday-monero-memes-qz1mao*

![37](/img/post/2022-09-01-the-monero-moon-57/37.png)  
*https://twitter.com/MoneroMemes/status/1387497756848234502/photo/1*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 57)](https://www.themoneromoon.com/p/the-monero-moon-issue-57)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
