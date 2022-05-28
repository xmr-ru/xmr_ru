---
title: "The Monero Standard #14 (18 мая 2022 — 25 мая 2022)"
date: "2022-05-25"
categories:
  - "Новости"
tags:
  - "The Monero Standard"
thumbnail: "img/post/2022-05-25-the-monero-standard-14/01.png"  
lead: "The Monero Standard — это еженедельный информационный бюллетень от p2p торговой платформы LocalMonero обо всём, что касается Monero."
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

_Опубликовано: 25.05.2022_
_Автор публикации: Kivojo_

## _Последние новости_

- Функция [Polyseed](https://github.com/tevador/polyseed) была [включена](https://github.com/feather-wallet/feather/pull/17) в [Feather Wallet](https://featherwallet.org/). Она позволяет создавать кошельки с мнемонической фразой длиной 16 слов и сохраняет дату создания кошелька, чтобы затем восстановить его на основе такой мнемонической фразы.
- Напоминаем, что 8 июня начинается [постэмиссия Monero](https://localmonero.co/knowledge/monero-tail-emission).
- Сообщаем о выходе версии [v1.2.0](https://libredd.it/uveju6/) Shruum Wallet. Не забудьте [добавить](https://f-droid.org/en/tutorials/add-repo/) соответствующий [репозиторий](https://mayumi.one/fdroid/repo?fingerprint=8D4981D23E8C15CEAC658681A7545B95E328759058F9DDA545CE557D643B7935) в клиент [F-Droid](https://f-droid.org/).
- Также сообщаем о [выходе](https://github.com/m2049r/xmrwallet/releases/tag/v2.4.3) версии v2.4.3 Baldaŭ Monerujo. В новой версии добавлена поддержка Ledger Nano S Plus.
- [Вышли](https://github.com/m2049r/xmrwallet/releases/tag/v2.4.3) новые версии Cake Wallet v4.4.1 и Monero.com v1.0.6.
- Pluja [сообщает](https://libredd.it/uvgmrb/) о выпуске новой версии [ISeeYour.Cash](https://iseeyour.cash/), поискового движка для сканирования профилей в социальных сетях с целью определения наличия BTC, ETH или XNO у пользователей.

## _Забавные факты / руководства_

![03](/img/post/2022-05-25-the-monero-standard-14/02.png)  

_Руководство по майнингу с помощью P2Pool_

[P2Pool](https://p2pool.io/) позволяет заниматься не требующим доверительных настроек / разрешений майнингом в блокчейне, не допуская злоупотребления мощностью хеширования в блокчейне. Благодаря интеграции P2Pool в официальный GUI-кошелёк Monero количество майнеров в блокчейне mini-p2pool (блокчейн для майнеров с низкой мощностью хеширования) достигло приблизительно 2000. В этом руководстве я расскажу вам, как заниматься майнингом с помощью P2Pool и как таким образом поспособствовать децентрализации сети и заработать несколько любимых Monero.

P2Pool сочетает в себе преимущества пула и соло-майнинга. При этом вы также часто получаете выплаты, но уже полностью контролируете мощность хеширования и узел. Вам необходимо скачать [последнюю версию](https://getmonero.org/downloads/) GUI-кошелька Monero, выбрать Advanced Mode (Продвинутый режим) во вкладке Mode Selection (Выбор режима), настроить свой кошелёк, в разделе Daemon Settings (Настройки демона) выбрать опцию Start a node automatically in background (Автоматически запускать узел в фоновом режиме). Как вариант можно использовать совместимый с P2Pool удалённый узел, p2pmd.xmrvsbeast.com или myxmr.net на RPC:18081 и ZMQ:18083. После синхронизации перейти в продвинутые настройки Advanced → Mining (Продвинутые → Майнинг) и выбрать P2Pool в Mining Mode (Режим майнинга) (выбор блокчейна: Mini, если мощность хеширования ниже 50 kH/s).

Обязательно ознакомьтесь с этим [материалом](https://localmonero.co/nojs/knowledge/p2pool-decentralizing-monero-mining), связанным с P2Pool и опубликованном в базе знаний LocalMonero.

## _Предприниматели (принимающие Monero)_

_Служебная директория KYCNot.Me_

[KYCNot.me](https://kycnot.me/) — это директория, предназначенная для бирж и предпринимателей, не следующих правилу KYC (знай своего клиента). Страница [Service](https://kycnot.me/services) (Сервис) этого сайта является богатым источником информации, благодаря которой вы сможете потратить свои Monero.

## _Примечательные проекты_

*Как помочь Monero?*

* [MoneroOutreach.org](https://monerooutreach.org/) опубликовали [очень подробную статью](https://www.monerooutreach.org/stories/getting-started-helping-monero.php), ознакомившись с которой, новички смогут узнать, как они могут помочь и развить идеи и саму философию Monero. Рекомендуем ознакомиться. Также обязательно прочитайте [эту статью](https://localmonero.co/nojs/knowledge/contributing-to-monero), добавленную в базу знаний LocalMonero.

* Веб-сайт [Monero Bounties](https://bounties.monero.social/) является подробным, понятным и актуальным источником информации о проектах Monero.

* [Требуется помощь в тестировании на предмет наличия ошибок в новой основной версии Monero](https://libredd.it/uqznue/).

*Прочее*

* [LibRedirect](https://libredirect.github.io/) — это бесплатное программное расширение для всех основных браузеров (в настоящее время доступно для Firefox и Edge в их собственных магазинах). Оно служит для перенаправления вас на обеспечивающие приватность сервисы, альтернативные многим популярным онлайн сервисам, таким как [YouTube](https://yewtu.be/), [Reddit](https://libredd.it/), [Twitter](https://nitter.net/), [Wikipedia](https://wikiless.org/) и многие другие. Репозиторий расширения на GitHub можно найти по этой ссылке. Следует отметить, что разработчики Tor Browser не советуют устанавливать какого-либо расширения в свой браузер, но с [LibreWolf](https://librewolf.net/) и [Brave](https://brave.com/) всё должно быть в порядке.

* [Monero Art Fund](https://monerochan.art/) является совместной попыткой художников и дизайнеров по созданию великолепных образов MoneroChan, девушки аниме, ставшей маскотом Monero. Если вам нравится то, чем они занимаются, и вы хотите, чтобы они продолжили работу, вы можете внести свои пожертвования. В этом новостном бюллетене мы воспользовались результатами их трудов, потому что сами мы слишком ленивы :)

## _CCS идеи и предложения_

*Идеи*

- [Финансирование разработки jeffro256 (частичная занятость, 3 кв. 2022)](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/319)
- [Улучшение Moneroj.net, написание статей и сопровождение (3 месяца)](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/318)
- [Обновление исследовательских вычислительных средств](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/317)
- [Разработка бизнес-кита Monero](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/311)
- [Patronero — опенсорс проект для сбора пожертвований путём майнинга](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/310)
- [Перевод GUI-кошелька, CLI-кошелька, сайта Monero, руководств по поведенческой экономике, криптовалютным рынкам (субтитры), Moneropedia, руководства пользователя на греческий язык](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/296)
- [Стратегия экспансии Monero в Афганистане](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/282)

*Запросы о финансировании*

- [Создание новых анимированных видео](https://ccs.getmonero.org/proposals/savandra-videos-for-monero.html)

*Запросы о финансировании работы над Monerujo*

* Отсутствуют

## *Мем недели*

![03](/img/post/2022-05-25-the-monero-standard-14/03.png)

## _Познавательная страничка_

[Решаем проблему приватности Web3](https://spirobel.substack.com/p/solving-the-web3-privacy-problem).

## _Пожертвования и контактная информация_

Написание настоящего информационного бюллетеня является одной из моих обязанностей, и LocalMonero оплачивает эту работу. Однако если вы сочтёте, что бюллетень достаточно информативен и полезен, то вот адрес моего кошелька:  
`89gUNDWHpNBD59eqJHcyg9RRfZ9xPBqdXKgVhLiYonhtjFMtmKJDumCRD3EWvmXeogKs5Jh4jfnUhdyif2U3tbT3Liu7F3M`

Спасибо!

*Как со мной связаться*

Нашли что-то стоящее упоминания? Хотите отправить что-то для включения в следующий выпуск? Просто хотите поговорить о чём-то?

Вы можете связаться со мной через [XMPP](xmpp:hatchbacks@disroot.org) и по [электронной почте](hatchbacks@disroot.org). Связь по электронной почте крайне не приветствуется.

---

_Источник: [The Monero Standard #14: 18 May 2022 - 25 May 2022](https://localmonero.co/the-monero-standard/weekly/14)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
