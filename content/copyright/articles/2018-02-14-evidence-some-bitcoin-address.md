---
title: "Доказательство того, что некоторый код генерации адреса Bitcoin позволяет обнаружить приватные ключи"
date: "2020-02-14"
categories:
  - "Статьи"
tags:
  - ""
lead: "Привет. Спасибо, что делитесь этим материалом, это помогает привлечь внимание. Меня беспокоило то, что разместив где-то материал он мог остаться особо не замеченным."
pager: true
toc: false
sidebar: "right"
---

Также я пытаюсь сохранить анонимность, потому что не хочу чтобы меня обвиняли в том, что я распространил эту уязвимость, или как-то либо виновен в убытках какой-либо компании. Это просто интересная "техническая" история, поэтому, я решил поделиться ею с вами.

_**История начинается ниже**_

Я вернул 9 BTC пользователю reddit fitwear, который заявил, что они были украдены из его кошелька на blockchain.info.

У меня есть доказательство, что некоторый код генерации bitcoin адреса на практике использует приватные ключи, которые могут быть легко обнаружены на регулярной основе. Это сделано умышлено или по ошибке. Некоторые кошельки были скомпрометированы вероятно куском кода не вызывающим подозрения. Кроме того с 2014 года кто-то регулярно откачивал bitcoin из таких кошельков. Случайно они это обнаружили (как я) или сами внедрили код, я не знаю. Выглядит либо как умная закладка, либо как ошибка программирования. Это могло быть еще одним вредоносным кусочком кода, однако как я объясню ниже, мне кажется это маловероятным. Чтобы полностью понять, как это работает и как я это обнаружил, читайте далее.

### _Некоторые пояснения_

Я наблюдал за bitcoin с тех пор как впервые о нем услышал в 2011. Одна из вещей которая меня увлекала была возможность создать приватный ключ практически из всего, используя SHA256 (т.е. SHA256(пароль\фраза)). Это конечно не рекомендуется для получения закрытого ключа, поскольку поскольку, если вы можете придумать слово\фразу, кто-то другой тоже может придумать такую же, и вероятность кражи ваших bitcoin довольно высока. Наиболее безопасные закрытые ключи генерируются из случайной последовательности. Вероятность, что кто-то другой сможет сгенерировать такую же последовательность из 32 случайных байт очень близкая к 0, это очень маловероятно (учитывая ожидаемый срок жизни вселенной).

Если вы посмотрите в блокчейн, то обнаружите, что люди "играли" с цепочкой отправляя небольшое количество bitcoin на адреса, соответствующие закрытым ключам сгенерированным с использованием SHA256. Например, на SHA256 каждого слова из файла /usr/dict/words, имеющегося на большинстве систем UNIX, была отправлена небольшая сумма. Был сайт brainwallet.org, который облегчал задачу конвертирования фразы в закрытый ключ + публичный адрес (Код по прежнему доступен на github, но сайт удален) Попробуйте использовать фразу "i find your lack of faith disturbing" (я нахожу отсутствие у вас веры возмутительным), "these aren't the droids you're looking for"(это не те дроиды которых вы ищите) или "satoshi nakamoto"(сатоши накомото) как входящие данные для SHA256. Вы заметите, что на адреса соответствующие этим закрытым ключам были отправлены небольшие суммы (и выведены с них). Очевидно, что они имели место быть найденными. Оказывается таких адресов довольно много (просто попробуйте поизучать и вы легко найдете их). Тут ничего нового и это известно сообществу Bitcoin довольно давно.

Я всегда хотел попробовать найти не столь очевидные примеры "обнаружения" закрытых ключей. Что-то кроме SHA256 (слова\фразы). Поэтому я решил поохотится за "похороненными" Bitcoin сокровищницами. Возможно, у меня получится найти какой-то bitcoin адрес, намеренно скрытый кем-то, но, до сих пор не обнаруженный? Я посвятил этому некоторое время в начале июня 2017 года. Честно говоря я не ожидал найти многого, но был очень сильно удивлен тем что смог обнаружить. Я начал с написания программы для сканирования каждого блока в блокчейне. Она записывала каждый публичный адрес, который был когда либо использован (примечание: я сохранял не только адреса, баланс которых был больше ноля, я сохранил их ВСЕ, поэтому, считаю, что я совсем случайно обнаружил это). В то время их было около 290 миллионов, так что это не было трудной задачей.

### _Опыты​_

Далее следует описание моих экспериментов и почему я считаю это мошенничеством или очень плохой ошибкой программирования.

### _Опыт №1_

Первый эксперимент состоял в том, чтобы увидеть использовал кто-либо хеш блока как закрытый ключ. Это был действительно отличный способ "упаковать" 32 байта в вашей голове. Вам нужно будет только запомнить высоту блока (всего 6 цифр) и соответствующее 32-байтовое число будет навечно сохранено в самой цепочке!

Результат: Успех! Я нашел 46 адресов, на которые было отправлено несколько bitcoin между 2009 и 2016 годами. Как и ожидалось все они имели 0 баланс, скорее всего потому что владелец вернул их обратно или они были обнаружены кем-то еще.

Вот пара примеров. Можете использовать blockchain.info, чтобы убедиться, что эти шестнадцатеричные значения являются хешем блока, встречающимся ранее в блокчейне. Это произошло в середине 2016.

```
1Buc1aRXCqdh6r7PRYWPAy3EtVFw5Ue5dk 000000006a625f06636b8bb6ac7b960a8d03705d1ace08b1a19da3fdcc99ddbd

1KLZnkqU94ZKpgtcWCRs1mhqtF23jTLMgr 000000004ebadb55ee9096c9a2f8880e09da59c0d68b1c228da88e48844a1485
```

Все еще ничего опасного.

### _Опыт #2_

Примерно как и в моем первом эксперименте я искал адреса, которые были сгенерированы из merkle root, используемого как закрытый ключ. (т.к. я искал сжатые и не сжатые ключи, то каждые 32 байта выражались двумя адресами в моей базе)

Результат: Отлично! Я нашел 6 адресов, до середины 2016 года. Несмотря на то, что каждый найденный адрес имел баланс равный нулю (весьма ожидаемо). Мне просто доставляло удовольствие успеха!

Пример:
```
13bkBdHRovsBkjM4BUsbcDNr9DCTDcpy9W 6c951c460a4cfe5483863adacafad59e5de7e55876a21857733ca94049d7d10c
```

Подобно методам merkle root и хеш блока, id (идентификаторы) транзакций похоже тоже использовались в качестве закрытых ключей. Но меня до сих пор ничего не тревожило.

### _Опыт #3_

Мне стало любопытно, а что если кто-то использовал повторяющиеся SHA256 от простых слов. Зачем останавливаться на одной итерации, если можно сделать миллион? Кроме того, чем больше итераций вы сделаете, тем сложнее будет обнаружить ключ. Я нашел большое количество. Вот несколько:
```
Sha256('sender') x 2
18aMGf2AxQ3YXyNv9sKxiHYCXcBJeJv9d1 098f6d68ce86adb2d8ba672a06227f7d177baca3568092e4cda159acca5eb0c7

Sha256('receiver') x 2
1C3m5mFx6SjBCpw6qLqzM8izZArVYQ9B5u 6681b4b6aa44318e55a724d7135ff23d76eb75847802cd7d220ecaa8427b91d4

Sha256('hello') x 4
17UZ4iVkmNvKF9K2GWrGyMykX2iuAYbe1X 28b47e9b141279ea00333890e3e3f20652bbd7abc2b66c62c5824d4d6fe50ac9

Sha256('hello') x 65536
1Mi5mVANRNAetbJ21u2hzs28qCJC19VcXY 52fa8b1d9fbb264d53e966809ce550c3ab033248498da5ac0c5ab314ab45198e

Sha256('password') x 1975 (This one's my favorite, someone's birth year?)
13mcYPDDktHdjdq9LwchhU5AqkRB1FD6JE 6e8cdae20bef63d33cb6d5f1c6c9c954f3148bfc88ef0aa1b51fd8b12fa9b41c
```

Эти люди очевидно "хоронят" bitcoin. Ожидали ли они, что монеты будут изъяты или нет, мы никогда уже не сможем узнать. По моему мнению, эти способы довольно поверхностные и легко обнаруживаются.

### _Опыт #4_

Последний мой эксперимент, после которого я поверил в то, что кто-то регулярно выкачивал из какого-то сервиса bitcoin с 2014 года.

Взгляните на этот закрытый ключ:
```
KyTxSACvHPPDWnuE9cVi86kDgs59UFyVwx2Y3LPpAs88TqEdCKvb
```

Публичный адрес:
```
13JNB8GtymAPaqAoxRZrN2EgmzZLCkbPsh
```

В байтах закрытый ключ выглядит так:
```
4300d94bef2ee84bd9d0781398fd96daf98e419e403adc41957fb679dfa1facd
```

Выглядит достаточно случайно. Тем не менее, эти байты на самом деле sha256 от этого публичного адреса!
```
1LGUyTbp7nbqp8NQy2tkc3QEjy7CWwdAJj
```

Я обнаружил это перебирая SHA256 от всех публичных адресов, которые я собрал при подготовке опытов, затем просматривая эти адреса (из сгенерированных закрытых ключей) на предмет использования. Бинго! Адресов нашлось достаточно много. Я обыскал лишь малую часть и нашел десятки адресов. Я также обнаружил, что на эти адреса недавно были отправлены bitcoin (за несколько недель\дней до моего обнаружения)

Я спросил себя "Зачем и кому это надо"?

Сначала я подумал, что это был кто-то, кто хотел избавиться от проблемы запоминания двух частей большой информации, таким образом запоминая только одну из них. Может они имели одну основную комбинацию адреса\закрытого ключа, а остальные получены из нее? Мне казалось это очень вероятным. Вы можете продолжать делать так в цепочке и получать сколько угодно пар, запоминая только первую комбинацию. Но я отбросил это предположение по одной простой причине; bitcoin поступившие на этот адрес были выведены за минуты или ещё быстрее. Если кто-то генерировал эти закрытые ключи для себя, то почему все монеты были почти мгновенно выведены во всех случаях, которые я видел?

Вот еще несколько (полный список в конце этого документа):
```
16FKGvEtu5KPMZqiTK4yjmsSZsJLyxz9fr from Sha256(1CRWfJdgVrfKLRS4G3vTMRhEQrCZZyHNMo)

1HwxL1vutUc42ikh3RBnM4v2dVRHPTrTve from Sha256(1FfmbHfnpaZjKFvyi1okTjJJusN455paPH)

1FNF3xfTE53LVLQMvH6qteVqrNzwn2g2H8 from Sha256(1H21ndKEuMqZbeMMCqrYArCdV8WeicGehB)
```

В каждом случае монеты были выведены в течении минут или секунд после поступления.

Гораздо более вероятно, что бот ждал появления этих монет. Кроме того, транзакции, на этих адресах продолжаются и по сей день! Но как бот может заранее знать, что этот адрес должен получить bitcoin?

### _Жульничество или ошибка?_

Именно в этот момент я сформировал теорию о том, что на самом деле происходит. Похоже на то, что кто-то внедрил вредоносный код в бэкенд системы майнингового пула, обменника или возможно, в код генератора кошелька. Они использовали публичную информацию, поэтому они могут обнаружить закрытые ключи и легко украсть монеты со стороны.

Но почему они используют Sha256(public_address)? Почему бы не использовать Sha256(public_address + некоторая супер сложная для угадывания случайная последовательность) или просто использовать вшитый в код адрес?

Что ж, и на этот случай у меня есть теория. Он (адресс) не может быть вшит в код, иначе он будет выглядеть подозрительно в репозитории исходного кода. Скорее всего, код был представлен кем-то, кто работает (или работал) на некоторую компанию, связанную с Bitcoin (обменник \ пул \ казино \ кошелек). Код, отправленный разработчиком в систему контроля версий, обычно проходит через процесс проверки кода. Гораздо проще скрыть невинно выглядящую SHA256 операцию среди миллионов строк кода, составляющих бэкенд. SHA256 используется всюду в Bitcoin и не выглядит подозрительно. Функция легко пройдет. Однако если отправить код, который выполняет SHA256(address + "secret_password1234xyz"), это будет выглядеть ОЧЕНЬ подозрительно. Я предполагаю, что кто-то проскользнул в рутине, в которой это ВЫГЛЯДИТ безвредно, но на самом деле уводит bitcoin к ждущему их боту.

На самом деле, это достаточно умно. Никто не может узнать адрес получателя заранее. Вам придется продолжить выполнение SHA256 на всех публичных адресах, которые когда либо использовались, чтобы поймать нужный в миллионной транзакции. Кто-то способен захватить эти монеты, просто наблюдая за адресом, который соответствует приватному ключу, сгенерированному из SHA256 одного из публичных адресов. Поддержка такой базы данных тривиальна, а просмотр информации довольно быстр.

Справедливости ради я полагаю, что это могла быть ошибка программирования. С переполнением буфера нет ничего невозможного. Мне бы очень хотелось взглянуть на код, если он будет когда либо найден.

Сделки ПРОДОЛЖАЛИСЬ вплоть до пары недель до того как я обнаружил это! Поэтому я написал бота, чтобы попытаться "поймать" транзакцию.

### _Взрыв мозга_

В течении ПЕРВЫХ 48 часов жизни моего бота, 19 июня целых 9.5 BTC были отправлены на адрес, для которого у меня был секретный ключ. В то время это равнялось, примерно, 23000 долларов США. Я был в шоке.

Вот этот адресс:
```
12fcWddtXyxrnxUn6UdmqCbSaVsaYKvHQp
```

Вот приватный ключ:
```
KzfWTS3FvYWnSnWhncr6CwwfPmuHr1UFqgq6sFkGHf1zc49NirkC
```

исходные байты, для которого были получены из SHA256 от:
```
16SH69WgJCXYXWV58sxjTxonhgBh5HCZTt
```

(что соответствует случайному адресу ранее использованному в блокчейне)

Но... Я недостаточно протестировал свою программу и она не смогла совершить транзакцию! 9.5 BTC торчали там целых 15 минут, прежде чем были собраны кем-то еще. Я, честно говоря, не думал, что первая сумма, попавшая под мой радар, будет такой большой. Другие примеры, которые я нашел после этой транзакции, были крошечными. Вполне возможно, что тот, кто переместил их с скомпрометированного адреса и был их владельцем. Может быть чей-то еще подчищающий бот берет только небольшие суммы большую часть времени, чтобы не привлекать внимание?

В этот момент я был уверен в том, что обнаружил что-то, что еще не было найдено. Я _мог_ взять те 9.5 BTC даже если это было известно другим. Также, если вы посмотрите историю этого аккаунта, 12 BTC было отправлено на него (и тут же выведено) всего месяцем ранее. Никто не заявлял о воровстве связанном с этим адресом (насколько мне известно)

Я исправил свою программу (на самом деле, как следует протестировал ее в этот раз) и запустил снова. Программа обнаружила больше транзакций (2 в течении следующих 48 часов). Я закодил бота игнорировать все что меньше 0.1 BTC поэтому я их не тронул. Я не хотел спугнуть кого либо тем, что я знаю о том что они делают (если это действительно так)

Прошло еще 3-4 дня и следующим срабатыванием мой бот обнаружил около 0.03 BTC (~$95USD). По какой-то причине они не были сразу выведены, как другие. На тот момент были выходные 4 Июля. Я тоже оставил их, прошло полных 7 дней прежде чем они были перемещены (не мной). Может это был законный владелец, а может бот. Мы никогда не узнаем.

Адрес был:
```
1LUqqMzaigWJTzaP79oxsD6zKGifokrh7p
```

исходные байты приватного ключа:

```
c193edeeb4e7fb5c3e01c3aebd2ec5ac13f349a5a78ca4112ab6a4cbf8e35
```

### _Интрига усиливается_

В то время я не осознавал, но последний перевод был на адрес, закрытый ключ которого не был сгенерирован из другого публичного адреса, как в первом случае. Вместо этого, адрес был сгенерирован из id транзакции! Я забыл, что заполнил свою базу закрытыми ключами сгенерированными из id транзакций при прошлых экспериментах. Я не пометил их и поэтому не знал, какие из SHA256 (публичный адрес), а какие из id транзакций. Я нашел несколько срабатываний за все время, но когда проверил балансы этих аккаунтов, они все были нулевые и я не придал этому значения. Но теперь моя база обнаруживает дополнительно транзакции и в такие адреса (основанные на id транзакции) тоже!

Ладно, возможно кто-то использует информацию из открытого блокчейна, чтобы гарантировать обнаружение закрытых ключей для адресов, с которых они собирали Bitcoin.

Занимательно, что я нашел связь между адресом 12fcWddtXyxrnxUn6UdmqCbSaVsaYKvHQp (SHA от публичного адреса) и переводом на 1LUqqMzaigWJTzaP79oxsD6zKGifokrh7p (id транзакции в качестве ключа). В истории обоих адресов вы увидите, что BTC попал на этот адресс: 1JCuJXsP6PaVrGBk3uv7DecRC27GGkwFwE

Кроме того, id транзакции (которая выступала ключом) был от предыдущей транзакции, которая положила BTC в скомпрометированый (обнаруживаемый) адрес изначально. Теперь все стало более ясно. Вредоносный код иногда использовал id последней транзакции, как закрытый ключ для предопределенного адреса назначения. Отследив 0.03 BTC в прошлое вы увидите, что я имею ввиду. В конце концов доберетесь до txid = закрытый ключ обнаруживаемого адреса.

Адрес 1JCuJXsP6PaVrGBk3uv7DecRC27GGkwFwE всего один из множества адресов. У меня есть причины верить, что их было большое множество за годы. Только этот относится к марту 2017 года. Вы можете видеть в истории этого адреса, когда они консолидировали их, добытые не честным путем, доходы в одну транзакцию для себя.

Я запустил бота на более долгий срок. В следующее срабатывание я получил для хешей блока, которые использовались как закрытые ключти (см. Опыт 1). Разумеется этот адрес также имел связи с 1JCuJXsP6PaVrGBk3uv7DecRC27GGkwFwE, адресом скопления денег!

Помните мой опыт с merkle root? Я считаю, что это тоже было частью схемы. Тем не менее пока у меня не было связи с этим конкретным адресом накопления. Как итог, я нашел 4 различных метода использования "обнаруживаемого" закрытого ключа.

Я удостоверился, что моя база заполнена всеми вариантами закрытых ключей: хеш блока, merkle root, id транзакции и Sha256(публичный адрес), и запустил своего бота. Были транзакции для всех 4 типов, опять же на крошечные суммы, которые я игнорировал. Но на этот раз я регулярно наблюдал как BTC изымается в небольших количествах. Иногда я видел как пролетали по 6 транзакций в день.

### _Как fitwear потерял (а затем вернул) 9 BTC_

12 ноября моя программа увидела 9 BTC поступивших на адрес, для которого в моей базе был закрытый ключ. Я также поискал не объявлял ли кто-нибудь себя владельцем этого адреса, но ничего не нашел. Я решил отправить небольшую сумму на популярный пазл адрес (puzzle address), чтобы привлечь внимание публики к транзакции, но анонимным путем (1FLAMEN6, я все еще пытаюсь решить его между прочим). Вскоре, после того как кто-то заметил, что сумма приза была превышена, я узнал о сообщении пользователя fitwear на reddit, в котором он говорил о воровстве, и я связал эти два события вместе.

Я связался с fitwear и вернул ему монеты, за исключением небольшой суммы, которую я отправил на ребус-адрес. Первоначальный ответ Blockchain.info, на его(fitwear) запрос в службу поддержки, был в том, что их система возможно была скомпрометирована. Как бы то ни было, если вы прочтете его сообщение, он принял все меры предосторожности, в том числе набрав ключ из его бумажного варианта, вместо копирования\вставки и он попутно использует 2FA (двухфакторную авторизацию).

В его случае, в августе 2017 он импортировал закрытый ключ от своего бумажного кошелька 1Ca15MELG5DzYpUgeXkkJ2Lt7iMa17SwAo в blockchain.info. И отправил тестовую транзакцию. В какой-то момент, между этим (12 августа) и 12 ноября, скомпрометированный адрес 15ZwrzrRj9x4XpnocEGbLuPakzsY2S4Mit попал в его онлайн кошелек как "импортированный" адрес.

Вместе мы связались с blockchain.info и я передал им информацию, которую описал выше. Их группа безопасности провела расследование, но не обнаружила доказательств того, что вина в их системе. Я полагаю, что в августе, его(fitwear) система была каким-то образом скомпрометирована и использована для импортирования ключа в blockchain.info, без его ведома. Или кто-то зашел в его аккаунт, импортировал ключ и ждал. Мне кажется вариант с вредоностным ПО\входом менее вероятен, потому что, на мой взгляд, выглядит все как попытка "спрятать код на самом видном месте". Вам нет необходимости использовать SHA256 (адрес) или хеш блока или txid или merkleroot, если вы используете вредоносное ПО или неавторизованный доступ. Вам как минимум надо использовать "соль" или малопонятный ключ с некоторой долей данных, известных только вам. Таким образом, только вы можете получить закрытый ключ (как упоминалось ранее). Тот факт, что была использована информация из блокчейна, указывает на то, что это может быть какая-то логика обработки транзакций. Кроме того, fitwear принял крайние меры предосторожности (вы можете почитать его пост для деталей). Происхождение подосланных адресов назначения остается загадкой.

Если это тот вариант когда код генерации некоторого кошелька делает это, тогда скорее всего имеет место быть вариант в котором мы видим транзакций "сдачи". Когда вы создаете кошелек, может быть сгенерировано 20 адресов. Все они должны быть случайными ключами. Если этот мошенеческий код, создает один из них таким образом (на основе строки публичного адреса, как один из предыдущих) то в какой-то момент ваша "сдача" будет возвращена ему путем "перебора" кошелька по списку.

15Z адрес fitwear'а не использовался до 12 ноября, когда он получил свои 9 BTC на него через blockchain.info.

Чтобы увидеть свзяь взгляните на это:

```
echo -n "1Ca15MELG5DzYpUgeXkkJ2Lt7iMa17SwAo" | sha256sum
9e027d0086bdb83372f6040765442bbedd35b96e1c861acce5e22e1c4987cd60
```

Это hex число является закрытым ключом для 15ZwrzrRj9x4XpnocEGbLuPakzsY2S4Mit !!!

fitwear утверждает, что он не импортировал ключ для этого адреса. Сгенерировал ли его Blockchain.info или он был добавлен через вредоносный код в браузере? Мы никогда не узнаем.

Ниже будет полный список других основанных на SHA256 адресов, которые имеют ту же проблему. Я считаю, что это происходит и с другими. Похоже небольшие суммы, которые обычно выводят, остаются незамеченными владельцами.

Что это значит для Bitcoin? Наверное ничего. Я считаю? что сама сеть Bitcoin безопасна. Тем не менее, пока люди вовлечены в сервис и его окружающие службы (пулы, обменники, онлайн\мобильные кошельки), но, всегда будет вероятность ошибки или мошенничества. Сама по себе сеть Bitcoin может "не требовать доверия", но все что касается периферии вокруг пользователей, конечно же так не может. Вы вынуждены использовать все эти сервисы для входа\выхода из сети. Так что даже с bitcoin все сводится к доверию.

Чтобы быть честным перед blockchain.info, только SHA256(публичный адрес) (в частности один) был найден в одном из их кошельков. Другие 3 метода описанные выше могут быть совсем не связаны. И все они могут быть (очень странным) программным багом.

Вот 100+ адресов, которые получили bitcoin, чьи закрытые ключи являются байтами результата SHA256 от другого публичного адреса. Большинство получено при сканировании, которое я делал для старых транзакций, а не во время работы моего бота. Blockchain.info сказали мне, что они были сгенерированы не их системой.

Кроме того, список адресов, который я предоставляю, это только та часть, через которые было проведено какое-то количество BTC. Вероятно более сотен лежат спокойно внутри кошельков людей, которые еще не были использованы.

Вот список:
```
1G2rM4DVncEPJZwz1ubkX6hMzg5dQYxw7b Sha256(1PoHkMExsXDDBxpAwWhzkrM8fabmcPt6f4)
1Kap8hRf8G71kmnE9WKSBp5cJehvTEMVvD Sha256(1LdgEzW8WhkvBxDBQHdvNtbbvdVYbBB2F1)
1LsFFH9yPMgzSzar23Z1XM2ETHyVDGoqd5 Sha256(1FDWY63R3M87KkW2CBWrdDa4h8cZCiov9p)
13eYNM5EpdJS7EeuDefQZmqaokw21re4Ci Sha256(1E7kRki9kJUMYGaNjpvP7FvCmTcQSih7ii)
1CcSiLzGxXopBeXpoNSchagheK9XR61Daz Sha256(191XapdsjZJjReJUbQiWAH3ZVyLcxtcc1Y)
1J9Gtk5i6xHM5XZxQsBn9qdpogznNDhqQD Sha256(16fawJbgd3hgn1vbCb66o8Hx4rn8fWzFfG)
1A17F9NjArUGhkkiATyq4p8hVVEh2GrVah Sha256(1Je3tz5caVsqyjmGgGQV1D59qsCcQYFxAW)
1GGFXUL1GoHcEfVmmQ97getLvnv6eF98Uu Sha256(1DCfq8siEF698EngecE69GxaCqDmQ2dqvq)
14XxBoGgaJd1RcV3TP8M4qeKKFL9yUcef1 Sha256(1Frj1ADstynCYGethjKhDpgjFoKGFsm5w5)
18VZKyyjNR8pZCsdshgto2F1XWCznxs86P Sha256(1FEwM9bq3BnmPLWw5vn162aBKjoYYBfyyi)
12fcWddtXyxrnxUn6UdmqCbSaVsaYKvHQp Sha256(16SH69WgJCXYXWV58sxjTxonhgBh5HCZTt)
19T6HNnmMqEcnSZBVb1BNA6PrAKd5P2qZg Sha256(1Frj1ADstynCYGethjKhDpgjFoKGFsm5w5)
1MWBsFxWJrNtK2cN2Vt7j3a9r5ubfn41nx Sha256(16era4SgYEcbZD1pu6oCBXGXjK2wSrePe8)
1Ns55SngRhshA8kEnyuQ9ELZZPN7ubYfQJ Sha256(1NiNja1bUmhSoTXozBRBEtR8LeF9TGbZBN)
13CnacdjvuuTJkCWrZf33yMrQh5aVX5B14 Sha256(1KPDwnrzJAfD2V4oiPf55WBTAi6UJDvMjN)
1MG1dTqtWVNqq3Qht88Jrie7SXp2ZVkQit Sha256(1UvM3rBJ8Sa1anQ8Du1mj5QZapFmWF7vH)
1DBXjdbMWXmgt81E1W7AYRANVPiq12LsGd Sha256(1Poi5SE42WVR2GKPrwp9U3wYqEBLN6ZV1c)
1GUgTVeSFd2L5zQvpYdQNhPBJPi8cN3i4u Sha256(1EjWVhiTyCdpTa29JJxAVLq27wP4qbtTVY)
1JQ2shEPzkd3ZL3ZQx7gmmxFLvyhSg14cb Sha256(1KEkEmadjTYHCiqhSfourDXavUxaiwoX7f)
125PcPD4QXzgDwNPForSFji8PPZVDr2xkp Sha256(1GRdTKgSq5sY3B4PiALPjKTXSXPXs6Ak7X)
1kN83e7WRtsXD7nHn51fwdEAi51qk5dEe Sha256(1JcsBzKio1curbu9AtxTySxddvT4MKT3Da)
1L5pzdXL4hhtMHNxFXHjjdhhSidY9kJVRk Sha256(1V8tWZw4J3G5kBgafGsfoVSNQEgkxDmeA)
1cQH5XCsezkKt9zpwjHizz8YJZudDSwri Sha256(1AYKSUqCtDX1E34q4YoFnjwWSj41huWgGG)
1DHWP6UjSKBBUR8WzTviWAGNgLfDc6V6iL Sha256(1MbzspFCdXjtqAUx3t6A11vzrk5c847mvE)
1EqSvLnMhbRoqZkYBPapYmUjMS9954wZNR Sha256(1XAeTJCaYJgoBDwqC1rhPhu3oXiKuMs9C)
1MJKz1M7dEQCHPdV5zrLSQPa4BGFAuNJyP Sha256(1BxzenHnSuKwqANALE5THeTCSRZkv3ReRP)
18VZG5Dr8bYJWadHUgh7kC4RPS1VsvH4Ks Sha256(1qA59Na3WysruJbCPoomryDRCtJ4f4aLu)
1CoyRECWJ4LHNiZAgAz9719chFkrDJuNMC Sha256(19o4Yjrd74qnZ3z87C67BShbbF4fSNHy8W)
1ERKXYeaCy97KPdJTRbWjJDVzMbStJYqCm Sha256(1DMwZeQJXfWToRRHr5uRiKeucwDWkWLvkm)
1mbcQaPzsaBoaYP4V6uwCA74BRPhroK3r Sha256(1KzSULbG3fRVjWrpVNLpoB6J62xYL42AdN)
1gHad7cKWDcVKFeKcLRW4FhFAyw2R7FQZ Sha256(1LFCEek8FobJRXb5YrzWJ6M2y8Tx2Xg3NB)
1DvtF6X5b9cBrMZa4Yff9tARCLqP5ZyB47 Sha256(14nuZCWe76kWigUKAjFxyJLFHQyLTsKXYk)
1LzGrd5QX1rG5fk7143ps9isUTEwGyzRJE Sha256(19cMyj9KqVq78yZe32CNhgpyuGLMwM9X8S)
153jMRXn251WyxT9nmJW2XDsFUJ648jyY5 Sha256(1PF2gQPPAwQDfTrSuNX6t8J381D7s3bGFu)
1EFBsAdysTf81k72v9Zqsj3NMuo6KoWD2r Sha256(1BBBvd9G5YThYVVMSGSxJzQvQiQm3WxJC2)
14mRxKmeEw9DCBbpR596FYmfZVdBD8MJxh Sha256(1PLpQDyqDUcpK6fWpRhkkFVBw4tSK4sHkS)
1Hg9pi75XWAT9pB3faXQFKKZbh98cbM5m Sha256(1JoshVWQDa7DzXqN3wQ9dbig5WEfaAzHcM)
1PcExYX3mUJ1rwa4aTLNJUpxqRLU8MxPXm Sha256(1LTZ9kaxRHBZH43eSmZ2KoGLHHUBV3P2S5)
1J9SzdYMZFsLqunQfPAswzogLNBitbREMD Sha256(1A7grBEjor6Sapj8KRbEGj2UrbnNt1Usxo)
1FNF3xfTE53LVLQMvH6qteVqrNzwn2g2H8 Sha256(1H21ndKEuMqZbeMMCqrYArCdV8WeicGehB)
1Q2a1ytfujskCEoXBsjVi1FqKWHegfFKwD Sha256(1LzGrd5QX1rG5fk7143ps9isUTEwGyzRJE)
1PfcpvjYUGu4yvpkEHmAKgDXtsLfSNyzvV Sha256(153jMRXn251WyxT9nmJW2XDsFUJ648jyY5)
1M2uEGihcwUPiRGETE7vF8kUiS2Z4rtV2Q Sha256(1HqQBiqgFK6ChJ2Vq7kbWRCbc73cjyNXv5)
1Kka5bgXvpHTNDsPmhLPHae2qcK9mLS2qS Sha256(1E3D7NabEX971uV2gXT47rWQwPm3zbmvd8)
17hMEK4i8Nsi56huBU4i9N4Gjiw5G6X5iG Sha256(1Nk6a8ZfN86gaHJifcF8iGahx4scCKkwF5)
1DT4Q4ocUFgekXvBqBM6kFmvQYB6Y4PnHo Sha256(19aNbfFfZEWwstuy97C1GsHHELNCxZSEYV)
1CSMVivJfFynvbZRrLFHVGnehpXLUjdGRc Sha256(1p4gsrzTc3mFAgJKYqMzhm6UsJzhgy1KX)
17SaWquajZZBRF5qz6HuXMRt6gvnrDyoqE Sha256(1C1KjGATUXP6L6nnGTAh4LQcnSyLt13XyB)
16eePivj1nTVvLpBGkmFoeGxNyMU7NLbtW Sha256(1K79KaFs4D6wqz1wjP1QoYiY18fw8N3bZo)
1PF2gQPPAwQDfTrSuNX6t8J381D7s3bGFu Sha256(1J9Gtk5i6xHM5XZxQsBn9qdpogznNDhqQD)
1GSkK6KBVSycEU57iK6fRvSXYJ4dgkkuNt Sha256(1JZwnSQz64N3F9D3E24oS4oGhSxMWDsXYM)
12eGusvkCcJb2GWqFvvE1BLDJ8pVX49fQv Sha256(197HxXUSehthdqXM6aEnA1ScDSCR7tQmP3)
134Kia3XhZV6oXE4EUvjc1ES8S8CY7NioU Sha256(1PVn2gxgYB8EcjkpJshJHfDoBoG8BntZWM)
1HMGSkDB9ZhRoUbSEEG6xR7rs9iPT2Ns5B Sha256(1E4yLggKcgHcpSKX336stXWgheNU2serVz)
13qsbkaJM7TkA5F2dsvHeGVQ7kCo74eGxh Sha256(1FAv42GaDuQixSzEzSbx6aP1Kf4WVWpQUY)
1Jsz6mahqVMJn2ayWzN6TfeWTti9tqfbSM Sha256(18AsiEQoLLKaF4Co1z4rxHyzJu9oqTVbFE)
1BwjscJC3P47uW5GXR7tjeHkdXQk6CuAFb Sha256(1JuP7JXhHabGLVAqp9TJj5N171qLVHrcVq)
17kYPYbELyVfMSYihD4YETJSZq5yCs3diM Sha256(1HzJPqLEpbeXiYhyoA8M8cuuds3FEAnw3B)
1C9HtVz7H8NArfV613wQNHs4PrK2oLZEYh Sha256(1EGeEk4YUrXyDL4zNXpWdqJopoVxs2vExJ)
16bEBNuc7JQ4QzyoFAkmxdVvW4wJqicjVN Sha256(12GvGqEQuQTW4Rr8dZ1o397KAYCMGWPYkq)
141V8fK9Kuofit8AXh9SLV9N9bLTfftETA Sha256(15nXjzf8EXy8Lji3czM1HAVw14mEKoEiTw)
19cMyj9KqVq78yZe32CNhgpyuGLMwM9X8S Sha256(17FaMY613bKfwhrdTv5PHnucSGTJBcw3k5)
1CRq6nj3a7vXdJJN2YSWdW6fVwydr6kqWs Sha256(1J1ZPHbbEwgcwniH3F7AgBeFZxQXJoKCGf)
1BVNt39u32LLkxMvBeBHXXNaTJqWe1Xcu5 Sha256(17iLALAyra1W5KSUjjkGN5LeUsWdeoQQx3)
1Mpw88XWQzLTZnq1eNs5SegZYGJu5Epky8 Sha256(1LeuaozTUT5UJX6DD4Q1VJsHh6aHpZ3YRU)
1LkwU9xbVroLkH9EvxDfmMnsCikQzaUv9S Sha256(16bEpxSc1FDyQDXR7ZYKbyyDDxzyaaCnNS)
1D97u8Pet8YmNwKaCPUXLyi4zk1HnLF5RQ Sha256(137XrofaWZhaZW2uB7eDsPjcwCNMTXVLot)
1KyUNmmJu3JjauVEZQUYLUEBg48GXXS1ii Sha256(17S3XjtEFXQoGdXnUjJJtGB1D7PTa9SsLZ)
1HwxL1vutUc42ikh3RBnM4v2dVRHPTrTve Sha256(1FfmbHfnpaZjKFvyi1okTjJJusN455paPH)
137XrofaWZhaZW2uB7eDsPjcwCNMTXVLot Sha256(1JvaK7jYWFNbDsJZLarXnq1iVicFW4UBv5)
1FXi6kEJjnZUBqpwjVJKPsgVHKag86k6qq Sha256(1FEYXtchFFJft6myWc6PyxLCzgdd8EHVUK)
1Gj2uRnxDztM7dTDQEUQGfJg4z5RtAhECh Sha256(1ESkNMa9Z37of4QdJmncvibrXxZ7suPjYm)
1JhWnRjRm7AhbvSBtEifcFL8DkEKQiWRZw Sha256(13Q8rTtdGUUt8Q8ywcEffj4oiNrY6ui3cu)
131XQfvE7E1NzdRQnE8XFmtkxWVRXTsb9q Sha256(1FLeb3zCVG63NYAMBiUoqKYgW1tUwgMMfF)
167dyxowdWwBdofck3WuAwvUpVfn2ewx8Q Sha256(1FFAdm2BWoCfTkTwFLJ4o3b5xG7cuRxbWb)
1CVunYyUpeCFcGAYdHrDNrXcQFBVU8gyo9 Sha256(1BEYFim8uoJ7FAZG6m1E1hqLwKjfVwnWU1)
14XAGCAeUxieSzvGK3TX915PJLvX54n2Pd Sha256(17XQfW1R66aRBNYyJMwzn7zLf3D6sZgda3)
1M5jhEDKQCYbMCXHgcRUmaxwqYmcbrEfGD Sha256(1AixDffKCd1cV1tz1sp8fwJQDEAYCWzQcR)
1HPnYqbMvV4bGRcpSP28mMyekhjKiudcFY Sha256(1C91NNyzXE1dBC4dDKjx6y5VnhihifrpCY)
15XWgB1biKGd1JyuYecobfFtfBcVt6Jnok Sha256(1268xJ8iYUdRxK2vArkyoa5es6bR99hjhR)
1NHvPBaxKFuDec27mWcyCf7szUUvNnfimK Sha256(1LdgEzW8WhkvBxDBQHdvNtbbvdVYbBB2F1)
1AoocdeZC64PaQ15Gbv1kXyYYnN8FWXAST Sha256(1Et9zapAxsBLJ3bvY7LDTuHif5cH7mZiBE)
1NWCqz8nr8ZRZt1zEKidyWcZDyNtK3THps Sha256(17Xok12pBFkXxNcE8J4gTSm3YKkatyX4ad)
1Lv6T9RegiNHpES1DHu6AasDcUqp2SeqLb Sha256(1LDqitspsYaiLH6AMW5EzJYuZG5vTGzRNg)
16FKGvEtu5KPMZqiTK4yjmsSZsJLyxz9fr Sha256(1CRWfJdgVrfKLRS4G3vTMRhEQrCZZyHNMo)
14JpZ9Bogo4p83xt6cKS1Fh1rLSFRat8PN Sha256(1FBxoyGYaC9GEKLokfyrHUbZyoZmmm1ptJ)
1BEYFim8uoJ7FAZG6m1E1hqLwKjfVwnWU1 Sha256(1PfcpvjYUGu4yvpkEHmAKgDXtsLfSNyzvV)
1P9ZZGDG1npYd4d7jiCfPya6LQGkF5sFm7 Sha256(1LFGKkDZ21FZVsBh1A1S5Xr6aXuV3x9N4k)
1JvaK7jYWFNbDsJZLarXnq1iVicFW4UBv5 Sha256(1LdkWzq9DxopPkY1hCmQ3DezenP5PQLNC3)
15RjQKt6D4HBn87QqgbyvhKFNDDjXncp8Y Sha256(1PhmMsdwamJA6soKw5mNMXxzGomHEHWY5P)
1G7B5eVnAQgeuGrKxcRnrmEqPLsjRkgnVF Sha256(1D97u8Pet8YmNwKaCPUXLyi4zk1HnLF5RQ)
192qwAD31JB9jHiAwaTDkd6teb2hLAkY3b Sha256(1PhqA75qNM23aH9zV3uWvUhDbdwcab6q5L)
13mbvCyxCYvATNzranCkQdpCT19VGpMFZa Sha256(1F3sAm6ZtwLAUnj7d38pGFxtP3RVEvtsbV)
1HJx3CqdaHAX6ZYRBHDvM5skg2Vh7GeZBD Sha256(1KrutzZZ7rth6D9wasfGz2oy9R6k1RCL9n)
1HBsFJ9VngvMjaKZjbFhNRaegkjF9NBEe Sha256(1CVunYyUpeCFcGAYdHrDNrXcQFBVU8gyo9)
1KiGdZ9TUeWyJ3DyHj7LQLZgjvMHd6j2DZ Sha256(18SV4DVmytRDYB5JBAFkewUbVAp6FRpi5c)
13FzEhD3WpX682G7b446NFZV6TXHH7BaQv Sha256(1E1rSGgugyNYF3TTr12pedv4UHoWxv5CeD)
1LVRWmpfKKcRZcKvi5ZGWGx5wU1HCNEdZZ Sha256(1CVPe9A5xFoQBEYhFP46nRrzf9wCS4KLFm)
1HhNZhMm4YFPSFvUXE6wLYPx63BF7MRJCJ Sha256(145Sph2eiNGp5WVAkdJKg9Z2PMhTGSS9iT)
1G6qfGz7eVDBGDJEy6Jw6Gkg8zaoWku8W5 Sha256(18EF7uwoJnKx7YAg72DUv4Xqbyd4a32P9f)
1MNhKuKbpPjELGJA5BRrJ4qw8RajGESLz6 Sha256(15WLziyvhPu1qVKkQ62ooEnCEu8vpyuTR5)
18XAotZvJNoaDKY7dkfNHuTrAzguazetHE Sha256(15SP99eiBZ43SMuzzCc9AaccuTxF5AQaat)
1HamTvNJfggDioTbPgnC2ujQpCj4BEJqu Sha256(14nuZCWe76kWigUKAjFxyJLFHQyLTsKXYk)
17iqGkzW5Y7miJjd5B2gP5Eztx8kcCDwRM Sha256(1MB3L1eTnHo1nQSN7Lmgepb7iipWqFjhYX)
15M7QfReFDY2SZssyBALDQTFVV1VDdVBLA Sha256(16bjY7SynPYKrTQULjHy8on3WENxCmK4ix)
1LgwKwv9kt8BwVvn6bVWj8KcqpP9JSP1Mh Sha256(1Q81rAHbNebKiNH7HD9Mh2xtH6jgzbAxoF)
1pmZwNDZjpuAqW3LjYYQCEjbQYBtSxzWc Sha256(13PctMqzyBKi5CpZnbastHQURrSRrow4yj)
1qA59Na3WysruJbCPoomryDRCtJ4f4aLu Sha256(1HBsFJ9VngvMjaKZjbFhNRaegkjF9NBEe)
19QBydCuMiY7aRTbkP2tb3KQJUWkTrr5Xi Sha256(1JwSSubhmg6iPtRjtyqhUYYH7bZg3Lfy1T)
11EuerTwe9rxtT3T56ykX5K7J3AksPzU3 Sha256(14PnZgX8ZDABJZ8RnatkK7DQzdpkwRRPX2)
13JNB8GtymAPaqAoxRZrN2EgmzZLCkbPsh Sha256(1LGUyTbp7nbqp8NQy2tkc3QEjy7CWwdAJj)
1Ads6ZWgRbjSCZ37FUqcmk82gvup1gQurB Sha256(1NbBTJQ5azGEA1yhGnLh39fE8YoEbePpCm)
1LWU4SbnqnfctAMbtivp2L98i8hSSCm7u7 Sha256(1MVqDAJo8kbqKfTJWnbuzvfmiUXXBAmX3y)
12B1bUocw8rQefDcYNdckfSLJ6BsUwhRjT Sha256(1Pjg628vjMLBvADrPHsthtzKiryM2y46DG)
12GZz1D1kdX3Fj7M87RFvqubam8iGrK77R Sha256(1Lu49ZKmGoYmW1ji3SEqCGVyYfEw7occ86)
13wY5CtwQhd7LYprEpFpkt1g9R7ErMkAwT Sha256(1NPSWKXdnHa17NWTU3J6nVkyogZjmAh7N6)
1Kc324Y6UUMffeYdtuXgzVC28Kx3U8cqQk Sha256(1HAQB99WfrV2ttRjttUPMzRi4R1uC2ftMy)
1Gwz14Cty45h3hZ4nCEno6jSdxtQn5bc7h Sha256(1PDgY5PkpBNCZVWKKAq3cbGyqvwwN91z4g)
1L2a5n9ar7e2v3Wz6NDFnxisigvR6urGaY Sha256(1KxUVU9DKfdaTLMnXBLS5BZRf56cFnRosk)
1KwUfu3gGk7n8Wz969tAztvvM4Mp4ZY57s Sha256(12XuaKzEheWbFJBno9QiV6kPCWrnWpUYTK)
13JNB8GtymAPaqAoxRZrN2EgmzZLCkbPsh Sha256(1LGUyTbp7nbqp8NQy2tkc3QEjy7CWwdAJj)
12fcWddtXyxrnxUn6UdmqCbSaVsaYKvHQp Sha256(16SH69WgJCXYXWV58sxjTxonhgBh5HCZTt)
1MkaTR3642ofrstePom5bbwGHbuQJmrnGD Sha256(1BynBc2YUAoNcvZLWi24URzMvsk7CUe2rc)
114LdauSAu2FTaR2ChPsPTRRhjYD9PZzn2 Sha256(144BV4Y7tgnetk5tDKAYTGS4mjprA75zJz)
1NzWscae8v3sKmTVJYwq8yhkizK8hUS5qP Sha256(1ENCBKFsqxJVCqR2TS1WfDV3rDi6zA8J6Y)
1FjEL7TBazaJN7WyND4uwq9wiaWDzfizkP Sha256(1PeCGFsJgqz8CcjGugGq5bPBiRDXUZHLUH)
1FP8j4zUPoJkpKwYpd8zYGHVaKygRHzx3d Sha256(1ERdvKTCxP1gZvdNndLKtYotW7qpR3xhuQ)
16nXouTPm5gVedr4Betb8KRWLSBtmXGUbD Sha256(16oTV1jZPJ5wm3QLhN96xVF7DchihmpL1k)
15ZwrzrRj9x4XpnocEGbLuPakzsY2S4Mit Sha256(1Ca15MELG5DzYpUgeXkkJ2Lt7iMa17SwAo)
```

Мой бот переместил монеты только с двух последних адресов. (никто не заявил права на 16nX). Все остальные переводы результат других людей, которые либо разгадали либо сами внедрили подосланные адреса (с 2014 года).

А вот некоторые свежие примеры закрытых ключей, основанных на другой информации из блокчейна (как указано, могут быть совершенно не связанны, но все равно появляются регулярно).

```
1LUqqMzaigWJTzaP79oxsD6zKGifokrh7p c193edeeb4e7fb5c3e01c3aebd2ec5ac13f349a5a78ca4112ab6a4cbf8e35404 txid
1FQ9AneLGfhFf9JT5m5sg5FaYFeJrGmJhS 00000000000000000045fa3492aee311171af6da7d05a76c6eaadab572dc1db9 Block Hash
1DhcPvYWBGwPFEsAJhXgdKtXX7FFGGeFVS 00000000839a8e6886ab5951d76f411475428afc90947ee320161bbf18eb6048 Block Hash
198MRUHD2cvgUTBKcnroqmoTSs4b8xyLH9 7dac2c5666815c17a3b36427de37bb9d2e2c5ccec3f8633eb91a4205cb4c10ff Markel Root
19FHVnoNYTmFAdC2VC7Az8TbCgrSWSP1ip 000000000000000000db717b4c076da2d1b9ff8ddbc94132e3a8d008a0fb62b9 Block Hash
1Lr2yEny7HYJkXdFgJ2D8zHyNH1uHMi4w4 2bedfd92a6136566bb858b2f0d223744a41a987c468356d069acc86f45bf68ac txid
1QBbjKxRk1jP36WYpFkJjgzhvVSDBMWjy2 f1599a1ced833d95a54aa38a1a64113d5f0a4db3cb613ef761180cab57155699 txid
1BFYNokepXjbb9Han2AGfSTNKNNU9vgAAn 533da7e41bd99550f63f152ef1e613f1a78e3bed12788664d536c6ec42b5e0aa txid
1MJtsgDNrrFWS3qxtrPr6BnQUdp1qPjyEm 216fb568589629b115b0ed8fc41fdf3219d9ab804c6ce5e53fbc581a88427c3f txid
14syDBvpGXS6PtWytkDJF2QACvSggEZ277 a7f4def1c7ff07d17b5dd58fc92f18ee2dbee6dc7654fd30a8653bd9d848f0a0 txid
1QBbjKxRk1jP36WYpFkJjgzhvVSDBMWjy2 f1599a1ced833d95a54aa38a1a64113d5f0a4db3cb613ef761180cab57155699 txid
1BkHAUcfrZLRLyXHiBn6XRoppPqSzuf8hE 805cd74ca322633372b9bfb857f3be41db0b8de43a3c44353b238c0acff9d523 txid
1CNgVFjAwHT7kc6uw7DGk42CXf1WbX4JQm 53d348ca871dc1205e778f4d8e66cfdadbd105782dba6688e9a0b4bdee4763e4 txid
1HjDAJiuJ8dda919xwKBqphhEwBVGfzMGt 0aad1b00a5227d9b03d33329a5a11af75c75c878a064c69b276063cbea677514 txid
1PDnrPSCw9eWTtJss4DhYoLTk4WUmZQdBi f87b08218888f97388218d3e2489962403f7eece98dd8b4733671edeb9ad1a7c txid
1MJp4z3ig498hNATfgHBAnLFhwoZpvw118 000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f Block Hash
```

Я думаю эта информация должна быть предана огласке, чтобы другие бэкенд системы подключенные к крипто сетям могли защититься от такой "спрятанного на виду" атаки. Как было сказано ранее, я честно собирался искать закопанные сокровища и наткнулся на чужой эксплойт. Спасибо yt_coinartist за распространение этого материала.

```
e8d064874c37ce44f13a880b93b548b83342c99e1530dd746322777f88397ed8
```
До скорой встречи. Ухожу в тень...

---

_Источник: [Evidence some bitcoin address generation code is using discoverable private keys](https://pastebin.com/jCDFcESz)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
