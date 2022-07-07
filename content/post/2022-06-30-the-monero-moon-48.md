---
title: "The Monero Moon (выпуск 48)"
date: "2022-06-30"
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

Разработчиками было принято решение отложить обновление сети Monero (хардфорк) примерно на две недели из-за задержки, связанной с аудитом multisig, проводимым третьей стороной. Мы надеемся, что обновление сети состоится на высоте блока 2 678 888 вместо 2 668 888, то есть на десять тысяч блоков позже. Данное решение обсуждалось на состоявшейся недавно встрече Исследовательской лаборатории Monero. [Monero Observer](https://monero.observer/meeting-log-summary-monero-research-lab-meeting-22-june-2022/) превосходно [осветили](https://monero.observer/meeting-log-summary-monero-research-lab-meeting-22-june-2022/) прошедшую встречу, а также опубликовали соответствующие ссылки на логи чата встречи.

![01](/img/post/2022-06-30-the-monero-moon-48/01.png)  
*Журнал встречи MRL - https://monero.observer/assets/logs/220622-mrl.log*

На случай, если вы ещё не в курсе, запланированное обновление сети Monero (хардфорк) является согласованным обновлением, согласованным сообществом Monero, призванным повысить уровень приватности и общей производительности. Всем пользователям необходимо обновить программное обеспечение. В рамках обновления будет реализован целый ряд новых функций, среди прочего:
- размер кольца будет увеличен с 11 до 16 в целях повышения приватности;
- будут реализованы теги просмотра, в результате чего время синхронизации сократится на 40%;
- после введения Bulletproofs+ размер транзакций уменьшится примерно на 7%, равно как и время верификации, которое также сократится на 7%.

Также вместе с новым программным обеспечением вскоре будет опубликован полный список улучшений и усовершенствований. Если вы хотите узнать больше о грядущем обновлении сети Monero, пожалуйста, ознакомьтесь с [этим постом](https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html) на официальном веб-сайте Monero.

![02](/img/post/2022-06-30-the-monero-moon-48/02.png)  
*https://www.getmonero.org/2022/04/20/network-upgrade-july-2022.html*

Если вы желаете помочь с обновлением сети Monero, достаточно просто уведомить о нём провайдеров кошельков и биржевых сервисов. Пожалуйста, сверьтесь с этим [контрольным листом](https://github.com/monero-project/meta/issues/690), чтобы все надлежащим образом обновили своё программное обеспечение и внесли соответствующие изменения.

![03](/img/post/2022-06-30-the-monero-moon-48/03.png)  
*https://github.com/monero-project/meta/issues/690*

Кроме того, вы можете помочь в тестировании и выявить ошибки в основной версии протокола Monero. Сделать это можно в тестовой сети. Соответствующие тестовые средства (tXMR) доступны абсолютно любому желающему! Дополнительную информацию, связанную с возможным оказанием помощи, можно найти в [этом посте](https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/), опубликованном garth_xmr.

![04](/img/post/2022-06-30-the-monero-moon-48/04.png)  
*https://www.reddit.com/r/Monero/comments/uqznue/help_test_the_upcoming_major_monero_release_for/*

Seth For Privacy также просит помочь в тестировании кода Monero. Он попытался сделать процесс как можно проще, опубликовав новый образ Docker, и теперь любой пользователь Ubuntu сможет просто воспользоваться ссылкой, приведённой выше, и начать тестирование. Если вы используете другую операционную систему, такую как Windows, [свяжитесь с Seth](https://www.reddit.com/r/Monero/comments/utzyyz/help_test_out_the_upcoming_monero_network_upgrade/), и он сделает всё возможное, чтобы помочь вам.

![05](/img/post/2022-06-30-the-monero-moon-48/05.png)  
*https://paste.sethforprivacy.com/?96466ca9ad3f3d90#4fTCXio2b3S6fX5b2YHffzY6zpYsj3bJrgZh7Gmi8ESC*

Monero уверенно движется к тому, чтобы повторно продемонстрировать самый высокий показатель по количеству транзакций за один месяц (второй раз с ноября 2021 года), когда их количество составит более 890 000, а также самое высокое соотношение транзакций (примерно 11,8%) в сравнении с Bitcoin.

![06](/img/post/2022-06-30-the-monero-moon-48/06.png)  
https://www.monero.how/

Рабочая группа сообщества Monero загрузила целый ряд видео с Monero Konferenco 2022, прошедшей почти две недели назад в Лиссабоне. Среди опубликованных видео вы найдёте презентации, посвящённые разработке атомных свопов XMR-BTC, децентрализации майнинга Monero и построении Web3 с помощью Monero. Ссылки на выступления можно найти [здесь](https://www.youtube.com/c/MoneroCommunityWorkgroup).

![07](/img/post/2022-06-30-the-monero-moon-48/07.png)  

![08](/img/post/2022-06-30-the-monero-moon-48/08.png)  
*https://www.youtube.com/c/MoneroCommunityWorkgroup*

Команда MyMonero объявила о выходе новой версии v1.2.5 своего мобильного приложения для пользователей iOS. Обновление позволит пользователям покупать XMR прямо в приложении! Обновление можно будет скачать на [MyMonero.com](https://mymonero.com/).

![09](/img/post/2022-06-30-the-monero-moon-48/09.png)  

pokkst разработал [Monero Decoy Scanner](https://github.com/pokkst/monero-decoy-scanner), позволяющий сканировать блокчейн Monero на предмет наличия транзакций, в которых в качестве ложных участников кольца были использованы определённые выходы, например, ваши собственные. Заходите на [GitHub](https://github.com/pokkst/monero-decoy-scanner), скачивайте и пробуйте сами!

![10](/img/post/2022-06-30-the-monero-moon-48/10.png)  
*https://github.com/pokkst/monero-decoy-scanner*

Джастин Берман ([Justin Berman](https://repo.getmonero.org/j-berman)) опубликовал свой окончательный отчёт по разработке Monero в рамках своего предложения CCS с февраля по май 2022 года. Джастин проработал более 480 часов и провёл большую часть этого времени за анализом кода. С отчётом можно ознакомиться по этой [ссылке](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/285#note_16904).

![11](/img/post/2022-06-30-the-monero-moon-48/11.png)  
*https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/285#note_16904*

MAGIC Monero Fund получил 50 XMR от щедрого анонимного жертвователя, и эти средства пойдут на улучшение экосистемы Monero и поддержку развития проекта. MAGIC Grants — это общественная благотворительная организация, которая выплачивает стипендии студентам, интересующимся Monero и другими криптовалютами, а также поддерживает различные критически важные криптовалютные платёжные инфраструктуры. В настоящее время фонд проводит внеочередные выборы нового члена комитета MAGIC Monero Fund. Заявки принимаются до 25 июля, а более подробную информацию о выборах вы найдёте здесь. Подробнее о фонде MAGIC можно узнать, перейдя по этой [ссылке](https://magicgrants.org/Special-Election-for-MAGIC-Monero-Fund/). Если у вас возникнет желание принять участие в их деятельности, свяжитесь с ними.

![12](/img/post/2022-06-30-the-monero-moon-48/12.png)  

[Parmicciano](https://www.reddit.com/user/Parmicciano/) создал «федеративное облако», платформу, позволяющую связать парк серверов с разработчиками. По сути, это платформа, которая предоставляет разработчикам необходимые вычислительные мощности за Monero. Вся дополнительная информация содержится в этом [посте](https://www.reddit.com/r/Monero/comments/vm3vsm/run_virtual_private_servers_for_others_and_be/).

Команда [Monerica.com](https://monerica.com/), директории, поддерживающей циркулярную экономику Monero, обратилась к сообществу за помощью, связанную с тем, чтобы пользователи смогли поспособствовать внесению изменений. Для получения более полной информации посетите эту [страницу](https://github.com/monerica-project/monerica).

![13](/img/post/2022-06-30-the-monero-moon-48/13.png)  
*https://github.com/monerica-project/monerica*

[Monero Observer](https://www.monero.observer/) опубликовали новый отчёт по разработке. Ознакомившись с ним, вы получите обширную картину того, что происходило в сфере разработки Monero в течение последней недели. Если вам интересны мельчайшие подробности, то сам отчёт вы найдёте [здесь](https://monero.observer/monero-dev-activity-report-week-25-2022/).

![14](/img/post/2022-06-30-the-monero-moon-48/14.png)  
https://monero.observer/monero-dev-activity-report-week-25-2022/

xmrqrcode.com, веб-сайт, позволяющий сгенерировать QR-код адреса Monero, является мошенническим веб-сайтом, так как созданные с его помощью QR-коды никак не связаны с вводимыми адресами. dsmlegend делится более подробной информацией по этому вопросу. Избегайте этого сайта и будьте бдительны при использовании QR-кодов для отправки или получения XMR.

![15](/img/post/2022-06-30-the-monero-moon-48/15.png)  

Настоятельно рекомендуется создать и использовать собственный узел или заняться майнингом. Это поддерживает надлежащий уровень безопасности сети. Вы можете заняться майнингом с помощью официального GUI-кошелька Monero, который можно скачать по этой ссылке, или в пуле, присоединившись к децентрализованному и не требующему каких-либо специальных разрешений P2Pool. Читайте достаточно информативный твит, опубликованный Лив Майкл (Liv Michael), ниже!

![16](/img/post/2022-06-30-the-monero-moon-48/16.png)  

### _Прочие новости_

Seth For Privacy принял участие в спонсируемом Cake Wallet подкасте What Bitcoin Did ([Что сделал Bitcoin](https://www.whatbitcoindid.com/podcast/privacy-on-monero-vs-bitcoin)), в котором обсуждались вопросы приватности, Bitcoin и Monero. Данный подкаст посвящён «исключительно Bitcoin», так что было довольно интересно наблюдать, как представителям сообщества Bitcoin приходилось признавать некоторые технические преимущества Monero и простоту её использования. Подкаст можно найти [здесь](https://www.whatbitcoindid.com/podcast/privacy-on-monero-vs-bitcoin) или на [веб-сайте What Bitcoin Did](https://www.whatbitcoindid.com/). Также можно просто воспользоваться твитом, размещённым ниже.

![17](/img/post/2022-06-30-the-monero-moon-48/17.png)  

Monero Talk опубликовали видео с Porcfest 2022, ежегодного мероприятия, организуемого [Free State Project](https://freestateproject.org/) и проводимого на открытом воздухе. В этом эпизоде участники Porcfest обсудили вопросы цены. Посмотреть видео можно [здесь](https://www.youtube.com/watch?v=02YCliSpnZA) или ниже!

{{< youtube id="02YCliSpnZA" autoplay="false" >}}  

Старый поклонник Bitcoin, организатор Satoshi Round Table (Круглый стол Сатоши) и кандидат в сенат США от штата Нью-Гэмпшир Брюс Фентон (Bruce Fenton) дал интервью Monero Talk, в котором неожиданно разоткровенничался в отношении Monero.

![18](/img/post/2022-06-30-the-monero-moon-48/18.png)  

Джастин Эхренхофер (Justin Ehrenhofer) обсудил Monero с Ноа из Whale Coin Talk в Telegram-канале последнего. Важен тот факт, что у канала более 22 000 подписчиков! Подробности обсуждения вы найдёте [здесь](https://t.me/whalecointalk).

![19](/img/post/2022-06-30-the-monero-moon-48/19.png)  

На YouTube канале [SovrinTV](https://www.youtube.com/channel/UCPwrMhBJWv1MEUceYHAuV-A) появилось видео с прекрасным обзором Monero, включающим историю проекта и его нынешнее состояние. Подача немного скучна, но содержание великолепно. При просмотре рекомендуется ускорить видео до 1,5x.

{{< youtube id="37JRvPL2ufI" autoplay="false" >}}  

Один из любимых Twitter персонажей сообщества Monero, Untraceable, недавно опубликовал отличный твит, посвящённый отсутствию свойства взаимозаменяемости у Bitcoin. Твит можно найти [здесь](https://twitter.com/DontTraceMeBruh/status/1540431708033540098?s=20&t=3e8d_Q-xORU-xBYrfgpPzA) или ознакомиться с ним ниже.

![20](/img/post/2022-06-30-the-monero-moon-48/20.png)  

Не знаете, как объяснить своему товарищу, что такое Monero? Твит, размещённый ниже, поможет вам!

![21](/img/post/2022-06-30-the-monero-moon-48/21.png)  

Вышел семнадцатый выпуск The Monero Standard. В нём рассказывается о всех последних событиях, так или иначе связанных с Monero. Ознакомиться с новым выпуском можно по этой [ссылке](https://localmonero.co/the-monero-standard/weekly/17).

Как сообщается, китайские власти использовали систему слежки за здоровьем (Health Code System) для ограничения вывода средств гражданами и ограничения их перемещения между городами. «Когда они [граждане] пытались вывести средства, «код здоровья» внезапно становился [красным](https://www.sixthtone.com/news/1010547/henan-bank-depositors-hit-with-red-health-codes). Это началось после того, как три банка центральной провинции заморозили депозиты на сумму 1,5 миллиарда USD, в результате чего сотням клиентов пришлось ехать в город Чжэнчжоу, чтобы попытаться получить свои деньги. Как выяснилось, что при попытке просканировать [QR-код здоровья](https://www.codastory.com/authoritarian-tech/china-vaccine-passport/) в магазинах города и в общественном транспорте тот становился красным, что означало, что граждане инфицированы вирусом. После этого некоторых граждан отправляли на [принудительный карантин](https://www.codastory.com/authoritarian-tech/shanghai-zero-covid-lockdown-food-escape-restrictions/), а некоторых задерживали местные власти». Более подробную информацию о случившемся можно найти по этой [ссылке](https://www.codastory.com/newsletters/infodemic/pediatricians-rally-to-dispel-medical-misinformation-on-tiktok/).

![22](/img/post/2022-06-30-the-monero-moon-48/22.png)  
*https://www.codastory.com/newsletters/infodemic/pediatricians-rally-to-dispel-medical-misinformation-on-tiktok/*

Один из пользователей Twitter утверждает, что Coinbase теперь запрашивает имя и адрес получателя средств, а также цель их вывода. Только после этого вы сможете получить свою криптовалюту. Пока это касается только граждан Нидерландов. Та же информация содержится в статье, опубликованной [BeInCrypto](https://beincrypto.com/coinbase-announces-new-kyc-requirements-for-dutch-users/).

![23](/img/post/2022-06-30-the-monero-moon-48/23.png)  

### _Мероприятия_

Сегодня, в четверг, 30 июня, в Лондоне состоится встреча сообщества Monero! Мероприятие будет проходить с 18:00 по 21:00 в пабе Dickens Inn. Вся дополнительная информация содержится в [этом посте](https://www.meetup.com/digital-privacy-decentralization-technology/events/286760673/).

![24](/img/post/2022-06-30-the-monero-moon-48/24.png)  
*https://www.meetup.com/digital-privacy-decentralization-technology/events/286760673/*

Встреча Исследовательской лаборатории Monero будет проведена в среду, 6 июля. Планируется обсуждение таких вопросов, как алгоритмы выбора ложных выходов и анализ аномального объёма транзакций. Соответствующие ссылки и дополнительную информацию о встрече, благодаря Monero Observer, можно найти [здесь](https://monero.observer/monero-research-lab-meeting-6-july-2022/). Встреча лаборатории MRL начнётся в 17:00 UTC на IRC-канале #monero-research-lab. Заглядывайте, если вам интересно, и увидите всё сами в режиме реального времени.

Встреча рабочей группы по разработке Monero пройдёт сегодня, в четверг, 30 июня, в 17:00 UTC на IRC-канале #monero-dev. Вы сможете наблюдать за ней в режиме реального времени. Вся дополнительная информация содержится в [этом посте](https://monero.observer/monero-development-workgroup-meeting-30-june-2022/).

Ниже вы найдёте все видео с Monero Konferenco 2022, опубликованные к этому моменту. Приятного просмотра!

{{< youtube id="4pj8ws005N4" autoplay="false" >}}  

{{< youtube id="vm_Kw5m_Osk" autoplay="false" >}}  

{{< youtube id="RSCziwwIvoc" autoplay="false" >}}  

{{< youtube id="LkBvVADqEWI" autoplay="false" >}}  

{{< youtube id="oxiJ7LBJfG0" autoplay="false" >}}  

{{< youtube id="getCBpyXGmM" autoplay="false" >}}  

{{< youtube id="cMZz2JGdXsU" autoplay="false" >}}  

{{< youtube id="mwWWem67W08" autoplay="false" >}}  

{{< youtube id="566950WnM1c" autoplay="false" >}}  

{{< youtube id="g_ehNdMsPIM" autoplay="false" >}}  

{{< youtube id="r_vH-NyOYAg" autoplay="false" >}}  

### _Биржи и предприниматели_

ShopInBit сообщают, что в мае-июне XMR стала второй наиболее используемой криптовалютой, заняв 27% от общего объёма. В начале этого года этот показатель составлял только 7%. Тренд совпадает с тем, на что указывали CoinCards.

![25](/img/post/2022-06-30-the-monero-moon-48/25.png)  

[Bitrequest](https://www.bitreques/), приложение для приёма криптовалют, которое может использоваться точками продаж или в качестве механизма оплаты в электронной торговле, теперь поддерживает Monero. Скачать приложение можно [здесь](https://t.co/TGObtFmiUw).

![26](/img/post/2022-06-30-the-monero-moon-48/26.png)  

Биржа Poloniex снова приостановила вывод XMR. Возможность была отключена в течение пяти месяцев, потом появилась на неделю, и вот снова!

![27](/img/post/2022-06-30-the-monero-moon-48/27.png)  

Пользователь Reddit [сообщает](https://www.reddit.com/r/Monero/comments/viuf82/psa_not_your_keys_not_your_monero_even_on_kraken/), что Kraken, одна из заслуживающих доверия и поддерживающих XMR криптовалютных бирж, закрыла его счёт после покупки XMR и призвала его отменить сделку. Многие члены сообщества Monero скептически отнеслись к этому сообщению, но даже несмотря на то, что Kraken является одной из самых надёжных бирж, поддерживавших Monero в прошлом, это должно послужить для всех очередным напоминанием, что если вы не сами храните свои Monero, то всё, что у вас имеется, по сути, это долговая расписка биржи, согласно которой та должна вам вернуть ваши XMR. Не ваши ключи — не ваши монеты.

![28](/img/post/2022-06-30-the-monero-moon-48/28.png)  
*https://www.reddit.com/r/Monero/comments/dl30m9/finished_up_a_new_pop_design_not_your_keys_not/*

Хотите купить или продать что-то за XMR? Посетите ветку [Friday Monero Market](https://www.reddit.com/r/Monero/comments/vjic20/friday_monero_market_thread_june_24_2022/) (Пятничный рынок Monero) на Reddit. Каждую пятницу пользователи субреддита Monero размещают там свои объявления о продаже/покупке и готовы торговать за Monero. Итак, ждём вас каждую пятницу по [этой ссылке](https://www.reddit.com/r/Monero).

[MoneroMerch.com](https://moneromerch.com/), веб-сайт, занимающийся продажей товаров, связанных с Monero, таких как футболки, худи, сумки для ноутбуков, чехлы для телефонов, кружки, носки и так далее, продаёт стикеры Monero по цене всего 1-2 USD за штуку. Доставка возможная в любую часть мира, а также сайт предлагает скидку в размере 5 USD при покупке товаров на сумму более 50 USD. 30% скидка предусмотрена для проектов Monero, связанных с системой CCS. Всю необходимую информацию можно найти [здесь](https://www.reddit.com/r/Monero/comments/vktiu5/moneromerchcom_we_might_be_selling_150_200/).

![29](/img/post/2022-06-30-the-monero-moon-48/29.png)  
*https://moneromerch.com/*

[Ziga Studio](https://zigastudio.com/), веб-сайт, занимающийся продажей постеров, футболок и прочих товаров, теперь принимает Monero. Сайт немного неудобен в использовании, но платёжный сервис XMR работает нормально.

Хотите выиграть несколько Monero? Заходите на [Monero Pot](https://moneropot.org/) и делайте ставки! Победитель определяется значением хеша первого блока месяца. Вводимый вами ID хешируется как sha(hash+id). Хеш вашего значения берется из предыдущего месяца. Побеждают хеши с наибольшим количеством совпадений.

![30](/img/post/2022-06-30-the-monero-moon-48/30.png)  
*https://moneropot.org/*

Также вы можете выиграть Monero, если будете следить за afungible в Twitter и примите участие в одном из проводимых им розыгрышей XMR. Ссылка на последний приводится ниже, но ранее пользователям, чтобы выиграть XMR, предлагалось решить несколько забавных головоломок.

![31](/img/post/2022-06-30-the-monero-moon-48/31.png)  

### _Краудфандинговая система сообщества (CCS)_

Несколько запросов о финансировании ожидают решения сообщества перед тем, как в Краудфандинговой системе сообщества CCS ([Community Crowdfunding System](https://ccs.getmonero.org/)) начнётся сбор средств на их реализацию. Пока что это просто запросы, но если они получат несколько положительных откликов со стороны сообщества, они будут перемещены в раздел Funding Required (Требуется финансирование), и вы сможете сделать соответствующее пожертвование через CCS.

![32](/img/post/2022-06-30-the-monero-moon-48/32.png)  

_**В настоящее время в CCS имеются следующие открытые предложения:**_

![33](/img/post/2022-06-30-the-monero-moon-48/33.png)  
*https://ccs.getmonero.org/ideas/*

_**Проекты CCS, требующие финансирования:**_

![34](/img/post/2022-06-30-the-monero-moon-48/34.png)  
*https://ccs.getmonero.org/funding-required/*

### _Торговля и биржевые спекуляции_

Ежемесячный график пары XMR/BTC продолжает демонстрировать 4-месячные свечи с самыми высокими минимумами, начиная с достижения нижней точки в начале 2022.

_**Показатели**_
- Общее количество Monero в обращении: 18 141 334 XMR
- Общая рыночная капитализация Monero: 2 103 095 350 USD
- Позиция в рейтенге Coinmarketcap: 28
- Цена XMR/USD: 115 USD
- Цена XMR/BTC: 0.00596 BTC
- Цена на LocalMonero.co: 119 USD
- Средний размер комиссии за проведение транзакции: 0.00011 XMR ($0.013)
- Хешрейт: 2.905 Ghash/s
- Распределение хешрейта между пулами для майнинга Monero:

 ![35](/img/post/2022-06-30-the-monero-moon-48/35.png)  
*https://minexmr.com/pools.html*

### _Для развлечения_

rbrunner7 написал научно-фантастический рассказ «Казначей» о Monero. Это уже 17-й короткий рассказ, посвящённый Monero. Найти и прочитать его можно по [этой ссылке](https://rbrunner7.github.io/treasurer.html). Полный список рассказов опубликован [здесь](https://www.reddit.com/r/Monero/comments/vjnfkt/the_treasurer_a_monero_fiction_short_story/).

![36](/img/post/2022-06-30-the-monero-moon-48/36.png)  
*https://rbrunner7.github.io/treasurer.html*

{{< youtube id="xHy6hbcgF0s" autoplay="false" >}}  

![37](/img/post/2022-06-30-the-monero-moon-48/37.png)  
https://www.reddit.com/r/Monero/comments/vkwn3c/monero_descending_from_heaven/

![38](/img/post/2022-06-30-the-monero-moon-48/38.png)  
*https://www.reddit.com/r/Monero/comments/vkwn3c/monero_descending_from_heaven/*

![39](/img/post/2022-06-30-the-monero-moon-48/39.jpeg)  
*https://twitter.com/LWhatsHisFace/status/1542342495836819456/photo/1*

![40](/img/post/2022-06-30-the-monero-moon-48/40.jpeg)  
*https://pixels.com/featured/monero-moon-astronaut-xmr-coin-blockchain-crypto-florian-dold-art.html*

![41](/img/post/2022-06-30-the-monero-moon-48/41.jpeg)  

![42](/img/post/2022-06-30-the-monero-moon-48/42.jpeg)  
*twitter.com/XMRArtFund/status/1533532271868661760/photo/1*

---

### _Пожертвования_

Если вам понравился информационный бюллетень и вы хотите получать ещё больше подобной информации, то скиньтесь мне на пару пива, пожертвовав немного Monero, которые вы не потеряли во время известного «происшествия с лодкой».
`88u3PpQH3zNDTWnrYgLVyiYihLL7aFT2GLRXCACezG3Q2jcoiEzW7UqZWV5Uov9iBc6DqdbjVuLxfgptdPGbm3wJTGvq8mT`

---

_Источник: [The Monero Moon (Issue 48)](https://www.themoneromoon.com/p/the-monero-moon-issue-48)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
