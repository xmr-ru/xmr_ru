---
title: "Аарон Фликерт - Spats: пользовательские конфиденциальные активы и токены"
date: "2023-06-23"
categories:
  - "Стенограмма"
tags:
  - "Monerotopia 2022"
lead: "Monero Konferenco 2023 #MoneroKon2023 Прага - День 1"
pager: true
toc: false
sidebar: "right"
---

{{< youtube id="_qE1CD3J8oM" autoplay="false" >}}

---

_**Аарон:**_ Меня зовут Аарон, и я собираюсь рассказать о Spats, новом протоколе, ориентированным на поддержку пользовательских конфиденциальных активов и токенов.

Прежде всего, это наша совместная работа с Арамом, который также присутствует здесь и является криптографом в проекте Firo, тесно связанным с Ереванским государственным университетом. Так что вы можете обсудить с ним некоторые аспекты этой работы. А немного позже он расскажет о Spark, протоколе, который был взят нами за основу.

И сразу традиционный отказ от ответственности. Я являюсь руководителем отдела исследований в Cypher Stack, исследовательской консалтинговой компании, и исследования, связанные со Spats, велись в рамках работы для Firo. Как обычно, все материалы носят исключительно информативный характер. Важно отметить, что результаты этого исследования пока не прошли официальной внешней экспертизы, так что протокол всё ещё находится в процессе разработки. Была осуществлена некоторая формализация, но работа пока ещё не завершена. И, очевидно, моё выступление не является советом специалиста.

И прежде всего, коротко о том, почему нас вообще должна волновать проблема конфиденциальных активов и токенов, и как всё это вписывается в рамки существующих протоколов.

Итак, существуют такие протоколы повышения уровня конфиденциальности, как RingCT, Seraphis и Spark, в основе которого лежат некоторые из тех же базовых идей, что и у Seraphis. Они уже позволяют делать некоторые действительно интересные вещи, которые нам в целом нравятся. Одна из них - скрытая адресация. Мы можем отделить адреса получателей от данных, связанных с монетами, которые генерируются и фактически содержатся в блокчейне - мы можем отделить их. Мы также можем обеспечить неопределённость траты монет, в результате чего в идеале становится непонятно, была ли конкретная монета потрачена в какой-то конкретной точке блокчейна. С помощью шифрования, обязательств и других криптографических методов мы также можем защитить такую информацию, как достоинство монет и прочие метаданные.

Но, что важно, эти протоколы поддерживают только один тип активов. Под этим я подразумеваю наличие единственного актива с определённым обеспечением, который может передаваться между различными пользователями системы. Нам же важно было понять, можно ли расширить эту систему, чтобы она поддерживала несколько типов активов, которые, что важно, имели бы независимое обеспечение?

Мы не говорим о создании каких-то непонятных видах обмена активов в блокчейне, требующих предоставления информации вроде данных о самом обмене, которые довольно быстро становятся нежизнеспособными. Нас интересует возможность поддержки нескольких типов активов, обеспечиваемых независимо друг от друга. То есть, чтобы при наличии активов A, B и C, вы могли бы передавать их по кругу, но при этом в идеале бы скрывалось, какой именно актив передаётся, а их обеспечение последовательно поддерживалось независимо от правил эмиссии, в которых говорится о том, как должен обеспечиваться актив.

Поэтому, в частности, мы хотим иметь возможность скрыть не только достоинство, но и тип актива в транзакции. Мы должны исключить возможность посмотреть на транзакцию и сказать, что осуществляется передача актива A, актива B или актива C. Мы просто должны видеть, что происходит передача какого-то актива, не зная при этом, что это за актив и какого он достоинства.

И отдельно, возможно, мы захотим поддержать, например, невзаимозаменяемые токены, что не являлось первоначальной идеей нашего исследования. Но когда мы дошли до определённого момента, кто-то спросил: "А не могли бы мы реализовать поддержку токенов?". И я ответил: "Не знаю". А через несколько часов я вернулся и сказал: "Да, можем". Я знаю, что многим не нравится идея токенов, потому что не нравится то, что они делают - путаница с блокчейнами и прочее. Но это же математика. Мы занимаемся чем-то просто потому, что нас интересует проблема. Если вы хотите использовать то, что было нами сделано, - отлично! Если нет, то вы вовсе не обязаны. Наш протокол может использоваться исключительно для поддержки активов, и совсем не обязательно токенов.

И в случае с невзаимозаменяемыми токенами мы также хотим убедиться в том, что в состоянии скрыть любой вид индексирования или идентификатор, представляющий токен в составе транзакции. Поэтому мы хотим, чтобы транзакции по возможности представляли собой единообразные блобы. На практике это невозможно, но это наша цель. Всегда ведь должна быть цель, верно?

Итак, как мы представляем достоинство актива в транзакциях сегодня? То есть, это уже существующие методы, но если вы не достаточно хорошо знакомы с тем, как работают такие протоколы, как RingCT, Spark, Seraphis, то мы указываем достоинство актива таким образом, чтобы поддерживались баланс и общее предложение, но делаем это безопасным способом, который не делает информацию общедоступной в блокчейне. Для этого мы используем так называемые криптографические обязательства.

Обязательство позволяет взять монету с некоторым достоинством v, которое является просто некоторым числом, и частично оно может быть указано, поскольку существуют и другие данные о монете. И для этого используется обязательство, которое скрывает значение, так что вы его не видите. Обязательство также привязывает это значение к монете, то есть, я не могу передать вам этот блоб в виде обязательства и позже сказать: "Нет, нет. На самом деле достоинство имеющейся у меня монеты гораздо, гораздо больше". Нет, это должно быть сделано уникальным способом. Таким образом, мы хотим иметь возможность привязать достоинство монеты к обязательству.

Для этого мы выбираем случайную маску или фактор ослепления, как его иногда называют. Мы смешиваем их с Monero и множеством других активов. Мы используем обязательства Педерсена, и я покажу, как они работают. Это некий блоб обязательств, который по сути создаётся с помощью простой арифметики эллиптической кривой, где у нас есть два элемента группы, G и H, и мы помещаем значение достоинства монеты в один слот, а маску - в другой. Криптография на эллиптических кривых работает превосходно, и мы получаем этот случайный на вид блоб, обязательство. И это обязательство уже можно эффективно использовать. Так, например, вы не можете просто взглянуть на обязательство и определить значение суммы или маску. Это называется сокрытием. Очень полезное свойство.

Но мы также можем продемонстрировать соответствие баланса транзакции, и сделать это не так, как в случае с Bitcoin, где вы просто смотрите на значения и проверяете, правильно ли складываются числа. Мы не знаем, что это за числа. Они скрыты в обязательствах. Но мы можем произвести арифметические действия с обязательствами. Это похоже на то, как это делается со значениями суммы. Вы демонстрируете, что баланс транзакции сходится с помощью доказательства с нулевым разглашением, что довольно удобно - используя суммы и разности обязательств, входов и выходов, вы можете предоставить что-то вроде доказательства Шнорра, чтобы продемонстрировать, что транзакция сбалансирована. Это очень простой криптографический метод. Если вы ранее не сталкивались с ним, просто поверьте мне на слово. Превосходно работает. Мы знаем, как это делается. Не раскрывая суммы или маски, можно криптографически показать, что транзакция сбалансирована.

Но как быть, если вы хотите безопасно реализовать поддержку сразу нескольких типов активов с независимым обеспечением в рамках одной транзакции? В Bitcoin на этот счёт были некоторые идеи, которые были изложены в документе под названием "Конфиденциальные активы". Довольно типичный теоретический документ. Но у меня была классная идея, как это реализовать. У неё были некоторые недостатки, о которых я не буду рассказывать, чтобы сэкономить время, но с удовольствием расскажу о них позже. Чтобы сделать всё, как задумано, чтобы достичь поставленных целей, придётся немного изменить всё решение.

Итак, в данном случае у нас есть несколько типов активов, которые мы хотим сделать взаимозаменяемыми. Это означает, что у нас есть монеты, которые являются делимыми и дифференцированными. Каждая монета должна выглядеть как любая другая монета. Это и есть взаимозаменяемость. Но другие виды активов, возможно, буду невзаимозаменяемыми, и вы их отношении я буду использовать термин "токены", чтобы отличить их от взаимозаменяемых монет. И эти токены в данном случае имеют фактические идентификаторы, поскольку являются невзаимозаменяемыми. Идентификатор принадлежит каждому отдельно взятому токену. И в этом случае нам нужно, чтобы они были дифференцированы, но только для получателей и обозначенных верификаторов, но не для блокчейна. Таким образом, во всех случаях нам нужно, чтобы транзакции были как можно более единообразными и не содержали ничего лишнего, чтобы как можно больше данных и метаданных было защищено до тех пор, пока они не будут раскрыты или пользователь сам не решит раскрыть их обозначенному верификатору.

Итак, Spats - это протокол, позволяющий достичь этих целей, будучи своего рода расширением существующих протоколов конфиденциальных транзакций. То есть, это не совсем новый протокол. Он предназначен для того, чтобы сделать что-то помимо того, что делают Spark, Seraphis. Вы даже можете попытаться сделать это с RingCT, если захотите. Но я бы не рекомендовал этого, поскольку для этого существуют более свежие протоколы, такие как Seraphis.

Не стану углубляться в подробности, поскольку у нас не так много времени, но идея заключается в том, чтобы взять эти обязательства по сумме, содержащие значение суммы и маску, и построить вокруг них ничего не представляющий собой блоб. Идея состоит в том, чтобы расширить эти обязательства, включив в них немного дополнительных данных. Одина из таких типов - тип актива, обозначим его как a, а другой - идентификатор. Обозначаем его как йота, а обозначение i просто взято из статьи. Это очень просто сделать с помощью обязательств Педерсена. Достаточно просто добавить в обязательство новые слоты, один из которых будет содержать тип актива, а другой - идентификатор, если вы его используете. Таким образом, мы определяем, что все активы, независимо от того, являются ли они взаимозаменяемыми или нет, имеют уникальный тип. Он не обязательно должен быть случайным. Это в принципе определяется протоколом. Вы можете просто использовать счётчик, который будет увеличиваться: один, два, три, четыре и так далее.

Взаимозаменяемые активы не станут использовать идентификаторы, потому что нам это не нужно. Идентификатору просто присваивается нулевое значение, чтобы повысить взаимозаменяемость. Но каждый из невзаимозаменяемых токенов будет иметь уникальный идентификатор в рамках своего типа. И опять же, он не обязательно должен быть случайным. Позже вы увидите, что безопасность от этого никак не зависит. Итак, теперь у нас есть типы активов и идентификаторы, которые вместе входят в обязательство монеты.

Итак, ранее у нас было обязательство, включающее в себя значение v и маску m. Теперь оно выглядит немного сложнее из-за добавления двух дополнительных компонентов - типа актива a и идентификатора йота. В случае с взаимозаменяемыми активами мы всегда присваиваем идентификатору йота нулевое значение, чтобы повысить взаимозаменяемость. А в случае с невзаимозаменяемыми активами, по техническим причинам, мы присваиваем значение, равное единице. И причина, по которой мы это делаем, заключается в том, что, по сути, это не позволяет разделить токен и передать такой невзаимозаменяемый токен двумя разными способами двум разным пользователям. Мы не хотим этого. Мы хотим, чтобы передача происходила атомарно. И оказалось, что если сделать значение v равным 1, то разделить его будет невозможно. Я не могу разделить 1 на меньшее целое значение. Я могу присвоить нулевое значение, но, как вы увидите позже, нам может понадобиться идентифицировать скрытые типы активов, используя нулевое значение v. Но сейчас это неважно. Идея заключается в том, что вы можете представить оба этих различных типа активов, взаимозаменяемые и невзаимозаменяемые, в рамках очень схожей концепции.

Так как же всё это воплотить? Сейчас в рамках таких протоколов, как Monero, существуют транзакции на базе монет определёнными значениями, которые могут создаваться в определённое время в рамках таких транзакций. При этом их номинал раскрывается. Это приходится делать, чтобы сеть смогла убедиться в том, что общая масса монет изменяется с чётко заданной скоростью. Таким образом, сейчас созданная монета со значением v может содержать доказательство Шнорра, подтверждающее, что она соответствует ожидаемому значению, определяемому правилами протокола. И при этом не обязательно раскрывать секретную маску m, и именно это защищает денежную массу.

И Spats, по сути, является расширением данной концепции, то есть, во время проведения операций на основе типа монет, операций создания монет, мы проверяем, соответствует ли новый тип создаваемого актива или идентификатора правилам консенсуса, которые, в конечном счёте, определяются нами, разработчиками. Сейчас при создании монеты или токена вы публично раскрываете тип, идентификатор и её номинал, что позволяет сети их проверить. Это гарантирует, что общая денежная масса будет верной для всех этих различных типов, независимо от того, являются взаимозаменяемыми или нет, в соответствии с правилами протокола, которые вы решите реализовать.

И что действительно хорошо, так это то, что по-прежнему поддерживается идея отделения активов от адресов. То есть мы по-прежнему можем использовать скрытую адресацию - всё работает точно так же.

Но что делать с такими вами, как транзакции перевода или траты средств? Есть одно простое правило. Суть его заключается в том, что криптографически мы хотим убедиться, что все потребляемые и генерируемые в транзакции активы, то есть ваши входы и ваши выходы, имеют один и тот же тип и идентификатор. Довольно простое правило.

Поэтому в случае с взаимозаменяемыми активами на данный момент мы можем использовать несколько монет разного типа, чтобы получить необходимое значение суммы в совокупности. Нам нужно иметь достаточно средств, чтобы потратить. И вы можете сгенерировать несколько монет одного типа, включая, конечно, как обычно, сдачу. И не забывайте, что мы присвоили идентификатору йота нулевое значение, чтобы все эти взаимозаменяемые активы выглядели одинаково.

В случае с невзаимозаменяемыми активами в транзакции будет передаваться только один токен. Помните: у этого токена есть ненулевой идентификатор йота. Он будет сохраняться на протяжении всех транзакций, чтобы вы могли доказать, что являетесь владельцем конкретного невзаимозаменяемого токена. В этом случае для единообразия вы также можете включить несколько фиктивных токенов с нулевым значением. Вот почему мы включили это правило, где значение v = 1. В этом случае правило работает превосходно.

Но есть одна загвоздка. Если вас не волнуют комиссии, то это просто красивая простая абстракция. Но, к сожалению, комиссии нас всё-таки волнуют. И проблема заключается в следующем. Как я могу взимать комиссию, например, с майнера, если тип актива защищён? Всё, что будет знать майнер, это то, что вы получаете какой-то актив. Возможно, ему всё равно, что это за актив, и вы тоже не хотите раскрывать его тип во время транзакции. И в любом случае он не будет знать, что это. Так что, к сожалению, обойти это невозможно. Поэтому Spats предусматривает довольно неудачный компромисс, который сводится ко второму простому правилу. Я соврал. На самом деле есть два простых правила. Сейчас транзакции, связанные с потреблением и созданием монет одного базового типа предполагают наличие комиссии. Например, Monero. Вероятно, Monero станет базовым типом актива, если такое расширение будет реализовано в Monero.

Таким образом, при проведении транзакции, по сути, происходит две вещи. Создаётся комиссия в виде фиксированного известного типа базового актива, который может быть согласован, а также с другой стороны, возможно, со стороны актива, передаются монеты или токены какого-то произвольного неизвестного защищенного типа активов. Майнерам не обязательно об этом знать, потому что в идеале им должно быть всё равно. Я не буду приводить здесь все доказательства, но расскажу вам о том, как на самом деле криптографически реализовать эти два простых правила.

Как всегда, ответом служат доказательства с нулевым разглашением - ZKP. Оказывается, мы можем добавить сюда несколько ZKP, абсолютно не требующим доверия способом. Это очень простые структуры доказательства. С точки зрения комиссии, вам нужно криптографически показать, что все потребляемые и генерируемые монеты на самом деле относятся к базовому типу актива. Поэтому мы присваиваем типу базового актива, опять же, Monero или какому-нибудь другому согласованному типу, нулевое значение. Я объясню, почему это необходимо, через секунду. Кроме того, мы также присвоили идентификаторам взаимозаменяемых типов активов такие же нулевые значения. И так мы криптографически доказываем, что необходимое условие соблюдено.

Также нам нужно продемонстрировать сбалансированность со стороны выплаты комиссии. И, опять же, мы уже знаем, как это сделать. Со стороны актива нам нужно показать, что все входы, потребляемые монеты и токены, и все выходы, генерируемые активы или токены - а со стороны актива, нам не обязательно знать их значения a и йота, поскольку это раскрыло бы определённую информацию - но мы хотим показать, что они одинаковы. И это также можно сделать с помощью продуманных доказательств с нулевым разглашением. И здесь мы тоже хотим показать сбалансированность со стороны актива. И мы знаем, как это сделать с помощью доказательств Шнорра.

В идеале это доказывает, что благодаря свойствам систем доказательств с нулевым разглашением утекает очень мало информации. Итак, со стороны выплаты комиссии мы хотим знать, какой актив используется, поскольку это согласованный актив. А со стороны актива мы не хотим знать, каков его тип, поскольку это приведёт к утечке данных и метаданных. И нам известно, как правильно построить доказательство. Каждое из них представляет собой доказательство подобное доказательству Шнорра, но обладающее несколькими довольно хорошими свойствами с точки зрения масштабирования. Так, например, размер каждого из этих доказательств совершенно не зависит от количества монет или токенов. Таким образом, мы получаем, постоянное, то есть наилучшее масштабирование. Верификация эффективна, а поскольку это доказательства типа доказательств Шнорра, возможна и надёжная пакетная верификация.

Доверительные настройки нам не подходят, и мы не хотим с ними связываться. Ничего этого не нужно. Их очень легко реализовать, а соответствующие доказательства безопасности очень просты. Так что, тут нет никакой безумной, а только понятная математика. Если вам интересно, существует решение под названием "сила запроса", которое была оформлено документально, и которым мы можем воспользоваться.

Есть также небольшое изменение, предполагающее небольшую модификацию доказательств с целью обеспечения поддержки векторных обязательств, но это очень легко сделать с помощью Bulletproofs и Bulletproofs+ путём внесения тривиальных изменений.

И как всё это скажется на эффективности при реализации в рамках протокола типа RingCT, Spark или Seraphis? Ну, это потребует модификации некоторых существующих доказательств, а также внедрения новых доказательств. Если подробнее, то размер доказательства диапазона изменится на незначительные 64 байта. Также со стороны актива будет необходимо добавить доказательство баланса, всего 128 байт, что не так уж плохо. А затем и доказательства эквивалентности, о которых я говорил, которые немного увеличивают размер со стороны базового актива. То есть нетривиальное количество байт, в данном случае, при нормальных обстоятельствах, 576 байт. Честно, не знаю, устроит вас это или нет.

Здесь необходимо отметить, что сюда не входят некоторые зашифрованные данные типов активов и идентификаторов, которые отправляются получателям, что является расширением того, что уже сегодня делается такими протоколами, как Monero. Но это зависит от некоторых правил протокола и структуры транзакций и предполагает минимальные изменения.

Что касается эффективности верификации, новые доказательства действительно быстры. Доказательства, подобные доказательствам типа Шнорра, отлично подходят для достижения нашей цели. Сложность верификации практически минимальна по сравнению с такими решениями, как доказательства диапазона, требующими больше времени для верификации.

А как при этом будут обстоять дела с миграцией? Мы не хотим создавать новые пулы монет и начинать с нуля с точки зрения обеспечения неоднозначности входов. Spats должен хорошо взаимодействовать с такими протоколами, как Spark, Seraphis или RingCT. И в идеале вам не придётся иметь дело с нелепыми миграциями из одного пула активов в другой новый пул активов, поскольку, при отсутствии надлежащей осторожности, это может привести к утечке информации, и связано с определённым риском. Но, к счастью, выбранное нами решение делает весь процесс предельно простым.

Как я уже говорил ранее, базовые типы активов определяются так, чтобы тип актива был равен нулю, чтобы его постоянное значение было нулевым. И в силу арифметического устройства обязательств это означает, что все существующие монеты, прежде чем вы примените к ним схему Spats, автоматически станут монетами Spats. Как если бы вам вообще ничего не пришлось делать. Всё делается с помощью небольшого уравнения, при использовании которого в случае добавления нулевых значений в обязательства, некоторые вещи исчезают. Это относится ко всем новым и существующим обязательствам. Так что решение очень надёжно. С такими доказательствами Spats совместимы все существующие монеты.

И поскольку у нас есть два простых правила, о которых говорилось ранее, и поскольку в случае с обязательствами мы используем некоторые новые доказательства ZKP, всегда будет существовать единый готовый к использованию пул активов. Нет никакой необходимости в проведении различия между фиксированными активами, а также между взаимозаменяемыми и любыми невзаимозаменяемыми активами. Все они будут принадлежать к одному пулу и выглядеть одинаково. Для ясности, всегда будет происходить утечка метаданных и данных транзакций, но мы, пожалуй, максимально приблизились к цели. Положительный момент также заключается в том, что Spats поддерживает реально чистую миграцию при добавлении к уже существующим протоколам.

И последнее, о чём бы хотелось буквально упомянуть — идея доказательств владения. Как правило, если вы владеете каким-то идентифицируемым, невзаимозаменяемым токеном, вероятно, в какой-то момент по той или иной причине вы можете захотеть доказать, что он принадлежит вам. Что при этом нам даёт доказательство владения? Ну, если подумать, оно обеспечивает несколько вещей. Вам нужно продемонстрировать, что обязательство, блоб в блокчейне, связанный с вашим токеном, указывает на тип актива, на который вы претендуете, и содержит идентификатор. Как вы помните, мы включаем это в обязательство и привязываемся к этим данным. Но нам требуется иметь возможность показать это криптографически. Нам также нужно показать, что вы действительно контролируете токен, то есть, что вам известны секретные данные, которые потребуются для передачи токена, даже если вы не собираетесь делать этого в момент доказательства. Вы также хотите показать, что не просто воспроизводите чьё-то доказательство, потому что если кто-то передаст мне доказательство владения, а я передам его кому-то другому, этот человек не должен считать, что токен принадлежит мне. Это не должно быть основано на доверии. Доказательства предназначены для использования в одном конкретном контексте.

И что важно, мы должны знать, что токен не был передан позже. Возможно, я владел им или контролировал его в тот момент, когда вы просматривали блокчейн. Но что, если я передал его позже? И первые две проблемы решаются просто путём использования доказательств типа доказательств Шнорра. Надеюсь, вы уже отметили, насколько хороши эти доказательства. Мы должны использовать их чаще.

А что касается воспроизведении доказательств, как оказалось, эту проблему также очень просто решить криптографически. Существует такой механизм, как связывание сообщений Фиата-Шамира. Он уже используется множеством различных протоколов. По сути, это означает, что вы можете включить в доказательство некое контекстное сообщение, и доказательство будет верифицировано только в том случае, если сообщение будет соовтетствовать. Таким образом, доказывающая сторона и верификатор могут легко обменяться запросами друг с другом. Это очень просто и не требует никаких затрат с точки зрения производительности.

Но последнее, о чём я говорил, нужно доказать, что токен еще не передавался. Вот тут-то и возникают проблемы. Это то, что мне не нравится, и работа в данном направлении ведётся. Продемонстрировать, что токен не был передан с момента предоставления и проверки доказательства, гораздо сложнее.

Один из подходов, который мне не нравится, заключается в следующем. Для токенов в том виде, в котором они существуют сейчас в протоколах типа Monero, протоколах типа Zcash, тоже характерно это. Они используют что-то вроде связующего тега, аннулирующей функции или образа ключа  - каждый называет это по-своему. Но, по сути, это скрытое представление того, чем является монета. Как известно, если в транзакции раскрывается связующий тег, образ  ключа или что-то подобное, то снова раскрыть это невозможно, не обозначив тем самым попытку двойной траты.

Поэтому один из подходов к построению доказательств владения заключается в эффективном раскрытии того, что представляет собой связующий тег, верификатору доказательства. Мне также нужно доказать, что я не передал вам какой-то случайный мусор, что связующий тег был сгенерирован, как положено. Это несложно сделать. И тогда верификатор сможет утверждать, что переданный мной, надлежащим образом сгенерированный тег не появился ни в одной последующей транзакции, что свидетельствовало бы о том, что токен был передан. Таким образом, если с точки зрения верификатора тег не появился в блокчейне, значит, токен по-прежнему контролируется доказывающей стороной.

К счастью, это скверное решение, поскольку если у верификатора есть связующий тег, даже если токен ещё не был передан, верификатор просто может придерживаться этого тега и наблюдать, когда тот появится в блокчейне, что будет означать, что токен был передан позже. И теперь верификатор не может сказать, куда деле делся токен или что-то ещё, но это приведёт к утечке важных метаданных, что само по себе плохо.

Поэтому лучше было бы доказать, что тег не появляется в блокчейне, не раскрывая его. А для этого нужны гораздо более хитрые методы доказательства, которые не так хорошо масштабируются, и над этим еще предстоит поработать. И доказательство владения могло бы стать неплохим решением. Так что если вы решите реализовывать протокол с поддержкой токенов, вы, вероятно, воспользуетесь им. Как я уже сказал, можно просто сделать что-то вроде взаимозаменяемых активов, и тогда все эти вопросы отпадут, и вам не нужно будет заботиться об их решении.

Итак, резюмирую: Spats - это новое решение, разработанное нами для работы с пользовательскими конфиденциальными активами и, по желанию, токенами. оно обеспечивает несколько хороших возможностей. Так, вы можете поддерживать взаимозаменяемые и невзаимозаменяемые типы активов единообразным и чистым способом. Вы можете сделать транзакции довольно единообразными, несмотря на наличие всех этих новых возможностей. Вы можете защитить данные типа активов, идентификаторы и значения суммы, чтобы они не были раскрыты при проведении транзакции никому, кроме получателей и обозначенных верификаторов. Вы можете взимать комиссию с фиксированного базового типа активов, что, вероятно, порадует майнеров или других подобных пользователей системы, в зависимости от того, как вы настроите свой протокол. Вы сможете доказать факт владения токеном, хоть и очень несовершенным с точки зрения вероятной утечки данных способом, который хотелось бы во многом улучшить. Системы доказательства очень просты, их безопасность легко продемонстрировать, и они довольно эффективны. Миграция происходит предельно чисто. Вам не придётся создавать новые пулы, чтобы перевести токены и монеты. Все монеты и токены могут находиться в одном большом пуле, независимо от того, являются ли они базовым активом или каким-либо другим не базовым взаимозаменяемым или невзаимозаменяемым активом.

Нами уже опубликован препринт. Он был размещён в архиве препринтов IACR, а также в репозитории GitHub. Так что вы можете увидеть, как протокол развивался с течением времени. Если вас заинтересовали слайды, вы также найдёте их там. И это моя электронная почта на случай, если кто-то захочет со мной связаться. И большое вам спасибо за внимание.