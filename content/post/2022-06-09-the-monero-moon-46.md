---
title: "The Monero Moon (выпуск 46)"
date: "2022-06-09"
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

Сегодня, 9 июня 2002 года, примерно в 00:31 UTC на высоте блока 2 641 623 запускается постэмиссия Monero. Вознаграждение за добавление блока теперь станет фиксированным и составит 0,6 XMR за блок. Размер вознаграждения является линейным, то есть темп инфляции Monero уже никогда не превысит 0%. Это делает Monero безинфляционной валютой в отличие от фиатных денег и централизованных криптовалют с известным объёмом денежной массы. sech1 [отметил](https://www.reddit.com/r/Monero/comments/v8a1f7/tail_emission_watching_page_is_updated/), что XMR, добытые до этого момента, не являются точным кратным 0,6 XMR. Причина заключается в том, что при добавлении полных блоков на вознаграждение налагается штраф, и майнер получает меньше 0,6 XMR. Это означает, технически постэмиссия будет в среднем приносить менее 0,6 XMR за блок.

В официальном аккаунте Monero в Twitter было опубликовано сообщение, в котором было описано, зачем Monero постэмиссия, как она работает и что это значит для рядовых пользователей. С твитом можно ознакомиться ниже.

![01](/img/post/2022-06-09-the-monero-moon-46/01.png)  

![02](/img/post/2022-06-09-the-monero-moon-46/02.png)  
*https://moneroj.net/compinflation/*

P2Pool.io обновили свой веб-сайт, и теперь процесс постэмиссии будет отображаться в режиме реального времени: пользователь сможет увидеть, сколько XMR было добыто, а также годовой темп инфляции Monero. На сайт можно перейти по [этой ссылке](https://www.reddit.com/r/Monero/comments/v8a1f7/tail_emission_watching_page_is_updated/).

![03](/img/post/2022-06-09-the-monero-moon-46/03.png)  
*https://p2pool.io/tail.html*

Ниже размещено видео доктора Кима, в котором разъясняется, что такое постэмиссия Monero, чем отличается её график от графика эмиссии Bitcoin, а также почему это правильно. Спасибо [Untraceable](https://twitter.com/DontTraceMeBruh) за то, что снова обратил на это внимание. Как было сказано, видео можно посмотреть ниже.

{{< youtube id="8quGD9W7B2I" autoplay="false" >}}  

Джастин Эхренхофер опубликовал обзор, посвящённый криптовалютным приватным транзакциям, совершённым в мае 2022. Доля Monero составила более 98,6% от общего количества! Читайте соответствующий твит ниже.

![04](/img/post/2022-06-09-the-monero-moon-46/04.png)  

selsta поделился новостями по разработке за май 2022. Весь этот месяц он усердно трудился над официальными кошельками Monero. Более подробную информацию можно найти [здесь](https://github.com/monero-project/monero/pulls?q=is%3Apr+author%3Aselsta), на GitHub.

![05](/img/post/2022-06-09-the-monero-moon-46/05.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/312#note_16680*

[ACK-J](https://github.com/ACK-J) отчитался по своей работе по гранту MAGIC, связанной с оценкой поверхности атаки кольцевых подписей при проведении атак с помощью машинного и глубокого обучения. Отчёт опубликован [здесь](https://github.com/MAGICGrants/Monero-Fund/issues/15#issuecomment-1145354923).

![06](/img/post/2022-06-09-the-monero-moon-46/06.png)  
*https://github.com/MAGICGrants/Monero-Fund/issues/15*

[UkoeHB](https://github.com/UkoeHB) на GitHub попытался развеять заблуждения, связанные Jamtis, схемой адресации, разработанной специально для Seraphis. Он опубликовал свой пост [здесь](https://github.com/monero-project/research-lab/issues/92#issuecomment-1146810255) и [здесь](https://www.reddit.com/r/Monero/comments/v4wq1g/seraphis_new_view_key_method_is_problematic_for/).

[unyieldinggrace](https://github.com/unyieldinggrace), также известный как fatalglory, опубликовал код своего [сканера транзакций Monero](https://github.com/unyieldinggrace/monero-tx-scanner). Как утверждает сам автор, «этот пакет может использоваться для сканирования транзакций Monero с целью определения того, принадлежит ли транзакция определённому ключу просмотра и публичному адресу. Всё работает с клиентской стороны, поэтому необходимость в том, чтобы делиться своим ключом просмотра или адресом со сканирующим сервером или каким-либо третьими сторонами, отсутствует. Основная цель состоит в том, чтобы люди смогли без каких-либо затруднений создавать программное обеспечение для торговых точек, которое работало бы в браузере или мобильном приложении». Код можно найти по этой [ссылке](https://github.com/unyieldinggrace/monero-tx-scanner).

![07](/img/post/2022-06-09-the-monero-moon-46/07.png)  
*https://github.com/unyieldinggrace/monero-tx-scanner*

[HackerIndustrial](https://github.com/Monero-HackerIndustrial) создал MoneroDice-WalletGen, офлайн генератор мнемонических фраз Monero Diceware, который делает это подбрасыванием кубиков. Чтобы узнать больше, перейдите по [ссылке](https://github.com/Monero-HackerIndustrial/MoneroDice-WalletGen).

![08](/img/post/2022-06-09-the-monero-moon-46/08.png)  
*https://github.com/Monero-HackerIndustrial/MoneroDice-WalletGen*

[vdo](https://github.com/vdo) опубликовал новую версию скрипта [xmr.sh v0.3.1](https://github.com/vdo/xmr.sh). Мастер настройки скриптов xmr.sh используется для настройки сервера с демоном узла Monero с Docker Compose, с выбранными вами сертификатами SSL для вашего домена, выбором сети, скрытым сервисом Tor, панелью Grafana и многим другим.

AnonimaUzanto приступил к анализу поля unlock_time транзакций и заявляет, что начиная с 2022 года наметилась интересная тенденция, связанная с указанием недействительного времени блокировки. Более подробная информация содержится в этом [посте](https://www.reddit.com/r/Monero/comments/v513x1/monero_unlock_time_analysis/).

![09](/img/post/2022-06-09-the-monero-moon-46/09.png)  
*https://github.com/AnonimaUzanto/monero_blockchain_analysis/blob/main/Unlock_Time_Analysis.ipynb*

[spackleXMR](https://www.youtube.com/channel/UCuiUb6sK6s9l0tQ8uZJobJQ) озвучил и опубликовал на YouTube раздел 2.3 «Криптография на эллиптических кривых» из книги «Monero с нуля». Видео можно посмотреть ниже или по этой [ссылке](https://www.youtube.com/watch?v=s4Wj-ijY9hQ). Это поможет вам составить представление о том, как всё устроено у Monero «под капотом».

{{< youtube id="s4Wj-ijY9hQ" autoplay="false" >}}  

Monero Talk пообщались с Элизабет Блинк (Elizabeth Binks), которая работает над реализацией возможности проведения атомных свопов Ethereum-Monero, которая уже тестируется в соответствующей сети Monero. Интервью можно посмотреть здесь или [ниже](https://youtu.be/sNE5j4TAuCc).

{{< youtube id="sNE5j4TAuCc" autoplay="false" >}}  

Paulred70 поделился видео, демонстрирующим, как без какой-либо оптимизации можно заниматься майнингом Monero с помощью XMRig на компьютере с установленной системой Windows 11 и процессором Intel 12900k. Видео приводится ниже. paulred70 [утверждает](https://www.reddit.com/r/Monero/comments/v6ybgo/try_mining_monero_on_windows_11_with_intel_12900k/), что добывает 0,001024 XMR в день.

{{< youtube id="tjSN1tnYOLg" autoplay="false" >}}

Майнер Monero [monerobull](https://www.reddit.com/r/MoneroMining/comments/v79j95/after_about_1_year_of_mining_i_finally_found_my/) добыл свой собственный блок спустя год майнинга. Блок был вычислен с помощью P2Pool.

![10](/img/post/2022-06-09-the-monero-moon-46/10.png)  

[xmrvsbeast](https://old.reddit.com/r/Monero/comments/v5dfdv/request_to_all_monero_public_node_operators/) попросил всех операторов публичных узлов Monero рассмотреть возможность реализации ZMQ на их узлах, которая позволит заниматься майнингом с помощью P2Pool. Соответствующий пост был [опубликован здесь](https://old.reddit.com/r/Monero/comments/v5dfdv/request_to_all_monero_public_node_operators/), и мы рекомендуем сперва ознакомиться с комментариями, чтобы убедиться, что это в полной мере подходит вам.

Также xmrvsbeast заявил, что тот, кто добавит в GUI-кошелёк Monero функцию, позволяющую пользователям без каких-либо сложностей заниматься майнингом посредством P2Pool с помощью удалённых узлов, получит [вознаграждение](https://bounties.monero.social/posts/67/p2pool-mining-in-monero-gui-wallet-via-remote-node). Более подробную информацию можно найти [здесь](https://bounties.monero.social/posts/67/p2pool-mining-in-monero-gui-wallet-via-remote-node).

![11](/img/post/2022-06-09-the-monero-moon-46/11.png)  
*https://bounties.monero.social/posts/67/p2pool-mining-in-monero-gui-wallet-via-remote-node*

Если вы являетесь или только собираетесь стать пользователем CLI-кошелька Monero, обязательно прочитайте эту великолепную [шпаргалку](https://monero.observer/monero-cli-wallet-cheat-sheet/), которой со всеми поделился 3RA на [monero.observer](https://monero.observer/). Содержащиеся в ней команды помогут вам максимально эффективно использовать наш CLI-кошелёк Monero.

![12](/img/post/2022-06-09-the-monero-moon-46/12.png)  
*https://monero.observer/monero-cli-wallet-cheat-sheet/*

Monero Observer также выложили новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то вы найдёте отчёт [здесь](https://monero.observer/monero-dev-activity-report-week-22-2022/).

![13](/img/post/2022-06-09-the-monero-moon-46/13.png)  
*https://monero.observer/monero-dev-activity-report-week-22-2022/*

### _Прочие новости_

Агентством Reuters опубликован [специальный доклад](https://www.reuters.com/investigates/special-report/fintech-crypto-binance-dirtymoney/) под заголовком «Как криптовалютный гигант Binance стал хабом для хакеров, мошенников и наркоторговцев» (How crypto giant Binance became a hub for hackers, fraudsters and drug traffickers). В докладе говорится, что на Binance было проведено транзакций на сумму, составляющую как минмимум 2,35 млрд USD, и эти деньги были получены в результате взломов, мошенничества с инвестициями и торговли наркотиками. В одном из разделов доклада Reuters заявляет, что хакеры использовали Binance для перевода украденных средств в Monero, чтобы «отмыть» их, а также, что люди используют Monero  в даркнете для покупки незаконных веществ. Полный текст статьи  Reuters можно найти по [этой ссылке](https://www.reuters.com/investigates/special-report/fintech-crypto-binance-dirtymoney/).

![14](/img/post/2022-06-09-the-monero-moon-46/14.png)  
*https://www.reuters.com/investigates/special-report/fintech-crypto-binance-dirtymoney/*

Представители Binance ответили на доклад [постом](https://www.binance.com/en/blog/ecosystem/the-crypto-money-laundering-myth-and-the-machine-working-overtime-to-sell-a-false-narrative-421499824684903964) под заголовком «Миф об отмывании денег с помощью криптовалюты и машина по сверхурочной продаже ложного нарратива» (The Crypto Money Laundering Myth and the Machine Working Overtime to Sell a False Narrative). В посте говорится о том, что «заинтересованные стороны продолжают распространять дезинформацию или намеренно вводить в заблуждение общественность, утверждая, что криптовалюта вовлечена в незаконную деятельность гораздо в большей степени, чем традиционная банковская система». Ответ Binance можно прочитать здесь а в размещённом ниже коротком отрывки из него сказано, что в 2021 году лишь 0,15% криптовалютных транзакций было связано с незаконной деятельностью.

![15](/img/post/2022-06-09-the-monero-moon-46/15.png)  
*https://www.binance.com/en/blog/ecosystem/the-crypto-money-laundering-myth-and-the-machine-working-overtime-to-sell-a-false-narrative-421499824684903964#the-crypto-money-laundering-myth-and-the-machine-working-overtime-to-sell-a-false-narrative*

[Ответ на статью](https://old.reddit.com/r/CryptoCurrency/comments/v6t3zg/binance_in_trouble_the_case_of_binance_vs_reuters/) Reuters можно найти на сабреддите r/cryptocurrency

![16](/img/post/2022-06-09-the-monero-moon-46/16.png)  
*https://old.reddit.com/r/CryptoCurrency/comments/v6t3zg/binance_in_trouble_the_case_of_binance_vs_reuters/*

Несколько отвлечённую, но всё же связанную со всем этим информацию опубликовало издание Wired. В их статье речь идёт о рынках даркнета и утверждается, что в качестве оплаты на них используется исключительно Monero. Статью можно прочитать [здесь](https://www.wired.com/story/alphabay-dark-web-market-ranking/).

![17](/img/post/2022-06-09-the-monero-moon-46/17.png)  
*https://old.reddit.com/r/CryptoCurrency/comments/v6t3zg/binance_in_trouble_the_case_of_binance_vs_reuters/*

The Monero Moon (и как я смею полагать сообщество Monero в целом) не приветствует использование Monero в незаконных целях. Следует отметить, что повышенный уровень приватности Monero может быть полезен для достижения самых разных и вполне законных целей, например, чтобы избежать корпоративной слежки, опасных отношений или же просто чтобы тайно купить подарок супругу или супруге. Приватность — не преступление.

Недавно в свет вышла [работа](https://arxiv.org/abs/2205.13882) под названием «Как «раскопать» миллион: валидация и расширение кластеров Bitcoin». Джастин Эренхофер [прокомментировал](https://www.reddit.com/r/Monero/comments/v6zu9t/resurrecting_address_clustering_in_bitcoin/) статью в связи с Monero. В работе демонстрируется, как различные типы транзакций в сети Bitcoin могут негативно отразиться на приватности пользователей, чего нет в случае Monero в силу обязательных обновлений и совершенствования сети. Комментарий Джастина и саму статью можно найти [здесь](https://www.reddit.com/r/Monero/comments/v6zu9t/resurrecting_address_clustering_in_bitcoin/).

![18](/img/post/2022-06-09-the-monero-moon-46/18.png)  
*https://arxiv.org/abs/2205.13882*

Издание The New York Times также опубликовало [статью](https://archive.ph/fqMp3) под заголовком «Насколько анонимен Bitcoin в реальности?» (How Anonymous is Bitcoin, Really?), который затем [был изменён](https://www.nytimes.com/2022/06/06/science/bitcoin-nakamoto-blackburn-crypto.html) на «Насколько Bitcoin не требует доверия в реальности?» (How Trustless is Bitcoin, Really?). Статью можно прочитать, перейдя по [этой ссылке](https://archive.ph/fqMp3).

![19](/img/post/2022-06-09-the-monero-moon-46/19.png)  
*https://www.reddit.com/r/Monero/comments/v3zcvw/why_monero_matters/*

Monero Talk выложили очередную запись с конференции Monerotopia 2022. Это видео, снятое на дискуссионной панели, посвящённой регулятивным и политике, в которой приняли участие директор Solidus Labs по политике регулирования и соблюдения норм Лиат Шетрет (Liat Shetret), советник по вопросам криптовалют и блокчейн-технологии компании Bradley Кэрол Р. Ван Клиф (Carol R. Van Cleef) и модератор панели, вице-президент по операциям Cake Wallet Джастин Эренхофер. Видео можно посмотреть [здесь](https://youtu.be/e1oywK2AUXU) или ниже.

{{< youtube id="e1oywK2AUXU" autoplay="false" >}}  

После перехода с Medium на Substack новостной дайджест The Monero Moon непрерывно и по нарастающей продолжает набирать подписчиков. Более подробная информация содержится в твите ниже.

![20](/img/post/2022-06-09-the-monero-moon-46/20.png)  

Seth for Privacy посвятил свой подкаст вопросам, связанным с Bitcoin и Monero.

![21](/img/post/2022-06-09-the-monero-moon-46/21.png)  

Предлагаем вашему вниманию юмористический [отчёт](https://willenrimer.com/downloads) под названием «Скандальный прогноз по динамике развития блокчейна Bitcoin» ([Outrageous Blockchain Trend Predictions](https://willenrimer.com/downloads)) от Willenrimer.

![22](/img/post/2022-06-09-the-monero-moon-46/22.png)  
*https://willenrimer.com/downloads*

Сообщается, что южнокорейские криптовалютные биржи исключают Litecoin из своих списков поддерживаемых валют из-за реализации сетевого обновления MimbleWimble Extension Blocks (MWEB).

Максималист Bitcoin и подкастер Питер Маккормак (Peter McCormack), у которого количество подписчиков в Twitter приближается к полумиллиону человек, в своём твите написал, что не считает Monero скамом.

![23](/img/post/2022-06-09-the-monero-moon-46/23.png)  

### _Мероприятия_

15 июня состоится встреча Исследовательской лаборатории Monero (MRL). Планируется обсуждение вопросов, связанных с алгоритмами выбора ложных выходов и анализом аномального объёма транзакций. Ссылки на эту и другую информацию, связанную со встречей, благодаря Monero Observer, можно найти [здесь](https://monero.observer/monero-research-lab-meeting-1-june-2022/#fn:14). Встреча MRL начнётся в 17:00 UTC на IRC-канале #monero-research-lab. Заходите, если интересно, и увидите всё сами в режиме реального времени.

Всего несколько часов назад в [Нью-Йорке](https://www.meetup.com/Monero-Enthusiasts-and-Doers-NYC/events/285273767/), [Денвере](https://www.meetup.com/Denver-Crypto-Group/events/285700599?utm_medium=referral&utm_campaign=share-btn_savedevents_share_modal&utm_source=link), [Лас-Вегасе](https://www.meetup.com/Vegas-Crypto-Meetup/events/285664379?utm_medium=referral&utm_campaign=share-btn_savedevents_share_modal&utm_source=link), [Чикаго](https://www.meetup.com/Monero-Chicago/events/285999977/), [Флориде](https://docs.google.com/spreadsheets/d/119TtA1I835gD2c6rwxHMTH48ihQwlWkSFs91BY-6NpE/edit), [Джорджии](https://www.reddit.com/r/Monero/comments/v2y1wx/georgia_monero_tail_emission_meetup/) и других местах началось Глобальное празднование (встреча по поводу) дня начала постэмиссии. Энтузиасты Monero празднуют окончание номинальной эмиссии Monero и начало постэмиссии со своими местными сообществами XMR. Monerotopia уже провела [прямую трансляцию](https://www.youtube.com/playlist?list=PLfJ_JjSwYaa9eIi2rFU7l0exz7MQJ1GLu) дружеских встреч членов сообщества Monero, проходящих по всему миру в честь начала постэмиссии Monero!

{{< youtube id="IaanwDoOb-k" autoplay="false" >}}  

В четверг 23 июня в 17:00 в Кейптауне, Южная Африка, в заведении под названием La Parada состоится встреча сообщества Monero. В свете хардфорка Monero, который состоится в июле, встречу посетят ведущие южноафриканские разработчики и адепты Monero. Более подробную информацию можно найти [здесь](https://www.meetup.com/cape-town-privacy-meetup-group/events/286391842/?utm_medium=referral&utm_campaign=announceModal_savedevents_share_modal&utm_source=link).

![24](/img/post/2022-06-09-the-monero-moon-46/24.png)  
*https://www.meetup.com/cape-town-privacy-meetup-group/events/286391842*

![25](/img/post/2022-06-09-the-monero-moon-46/25.png)  

Конференция [Monerokon](http://monerokon.com/) пройдёт 18-19 июня 2022 в Лиссабоне, Португалия. Местом проведения станет Arroz Studios. Monerokon станет фестивалем всего связанного с Monero, обеспечением приватности и финансовой технологией, и эта конференция должна стать ежегодным местом встречи сторонников приватности данных, шифропанков, учёных и философов. Следует отметить, что билеты на Monerokon 2022 уже распроданы, но, если повезёт, могут появиться и дополнительные билеты.

Организаторы Monerokon также ищут волонтеров, которые могли бы помочь с решением ряда задач на конференции. Так что, если вы готовы протянуть руку помощи, свяжитесь с ними, перейдя по этой [ссылке](https://www.reddit.com/r/Monero/comments/v0vsqa/monerokon_2022_call_for_volunteers_it_takes_a/).

![26](/img/post/2022-06-09-the-monero-moon-46/26.png)  
*https://cryptpad.disroot.org/form/#/2/form/view/RqXzBJnXRsLaSBA6cMdtU0+45fXUvWDhXxxTOF1WM+A/embed/*

Очередная плановая встреча по проведению MoneroKon 2022 состоится в субботу 11 июня 2022 года в 18:00 UTC на IRC-канале #monero-events.

### _Биржи и предприниматели_

[etw01](https://www.reddit.com/r/Monero/comments/v8946q/bring_da_beats_im_donating_1_xmr_to_the_next_big/) предлагает вознаграждение размером в 1 XMR любому, кто напишет музыку на тему Monero. Вся дополнительная информация изложена в этом [посте](https://www.reddit.com/r/Monero/comments/v8946q/bring_da_beats_im_donating_1_xmr_to_the_next_big/).

![27](/img/post/2022-06-09-the-monero-moon-46/27.png)  
*https://www.reddit.com/r/Monero/comments/v8946q/bring_da_beats_im_donating_1_xmr_to_the_next_big/*

### _Краудфандинговая система сообщества (CCS)_

Веб-сайт bounties.monero.social отблагодарил hennyh за старания. Подробности в этом [посте](https://monero.observer/hennyh-wins-xmrvsbeast-bounty-restoring-bounties-monero-social-functionality/), опубликованном [monero.observer](https://monero.observer/hennyh-wins-xmrvsbeast-bounty-restoring-bounties-monero-social-functionality/).

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![28](/img/post/2022-06-09-the-monero-moon-46/28.png)  

_**В настоящее время в CCS имеются следующие открытые предложения для финансирования:**_

![29](/img/post/2022-06-09-the-monero-moon-46/29.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![30](/img/post/2022-06-09-the-monero-moon-46/30.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

schwarg разместил пост под заголовком «XMRBTC: куда мы движемся?» ([XMRBTC Which way will we go???](https://www.tradingview.com/chart/XMRBTC/xNH7uJaz-XMRBTC-Which-way-will-we-go/)). Ознакомиться с ним можно по этой ссылке.

![31](/img/post/2022-06-09-the-monero-moon-46/31.png)  
*https://www.tradingview.com/chart/XMRBTC/xNH7uJaz-XMRBTC-Which-way-will-we-go/*

Тем временем [Dangermousebanana](https://www.tradingview.com/chart/XMRBTC/YzV0ixaf-XMR-I-am-bullish-on-privacy/) отмечает бычий тренд Monero и предлагает возможный фрактал цены.

![32](/img/post/2022-06-09-the-monero-moon-46/32.png)  
*https://www.tradingview.com/chart/XMRBTC/YzV0ixaf-XMR-I-am-bullish-on-privacy/*

_**Показатели**_
- Общее количество Monero в обращении: 18 132 2642 XMR
- Общая рыночная капитализация Monero: 3 392 327 274 USD
- Позиция в рейтенге Coinmarketcap: 26
- Цена XMR/USD: ~187 USD
- Цена XMR/BTC: 0.00620 BTC
- Цена на LocalMonero.co: 198 USD
- Средний размер комиссии за проведение транзакции: 0.00012 XMR ($0.022)
- Хешрейт: 2.803 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

![33](/img/post/2022-06-09-the-monero-moon-46/33.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

![34](/img/post/2022-06-09-the-monero-moon-46/34.png)   

![35](/img/post/2022-06-09-the-monero-moon-46/35.png)  

![36](/img/post/2022-06-09-the-monero-moon-46/36.png)  
*https://www.reddit.com/r/moonero/comments/v4adk3/monero_poster/*

![37](/img/post/2022-06-09-the-monero-moon-46/37.png)  
*https://boards.4channel.org/biz/thread/49464155*

![38](/img/post/2022-06-09-the-monero-moon-46/38.png)  
*https://boards.4channel.org/biz/thread/49464155*

![39](/img/post/2022-06-09-the-monero-moon-46/39.png)  

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 46)](https://www.themoneromoon.com/p/the-monero-moon-issue-46?s=r)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
