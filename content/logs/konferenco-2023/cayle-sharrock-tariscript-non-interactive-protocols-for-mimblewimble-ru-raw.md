---
title: "Кайл Шэррок - TariScript: неинтерактивные протоколы Mimblewimble"
date: "2023-06-25"
categories:
  - "Стенограмма"
tags:
  - "MoneroKon 2023"
lead: "Monero Konferenco 2023 #MoneroKon2023 Прага - День 3"
pager: true
toc: false
sidebar: "right"
---

{{< youtube id="9yjJsLw14r0" autoplay="false" >}}

---

_**Кайл Шэррок:**_ Добрый день! Мы выходим на финишную прямую, после чего сможем выпить по первому пиву. Некоторые - уже по третьему. Я видел.

Итак, "TariScript: неинтерактивные протоколы Mimblewimble", или, возможно, более подходящим названием было бы "Как мы добавили скрипты в Mimblewimble".

И сначала план моего выступления. Прежде чем говорить о TariScript, я должен рассказать о Mimblewimble и Tari. Здесь собрались люди из Monero, и, полагаю, не все из присутствующих знакомы с Mimblewimble. Поэтому мне придётся немного рассказать о Tari, о том, как этот проект связан с Monero, что делает его интересным, как работают конфиденциальные транзакции и почему в простой версии Mimblewimble сложно реализовать скрипты, а также, зачем они нужны в Tari.

Итак, Tari - это быстрый масштабируемый протокол приватных цифровых активов, майнинг которых происходит совместно с Monero. Это и есть наша основная связь. Вторым связующим звеном является основатель Tari, которым является никто иной, как fluffypony. Так что у этих двух проектов богатая история.

И судя по некоторым разговорам, в которых мне довелось поучаствовать в эти дни, слухи о гибели Tari были сильно преувеличены. Последние пару лет мы упорно работали над построении данного протокола на основе двух уровней.

Первый уровень - это, как мы называем его, Minotari. Это протокол, в основе которого лежит алгоритм доказательства работы, и который был построен на базе Mimblewimble. Он использует гибридное доказательство работы и 60% блоков вычисляются с помощью Monero.

А ниже находится второй уровень - сеть цифровых активов. Именно там задействуются смарт-контракты. Именно там находится всё самое крутое и интересное. Но сегодня я не стану говорить об этом. Я расскажу о том, как мы усовершенствовали Mimblewimble, чтобы обеспечить связь между первым и вторым уровнем.

Итак, Mimblewimble 101, что это такое? Mimblewimble - это, по сути, то же самое, что и Bitcoin. Это криптовалютный протокол, но использующий конфиденциальные транзакции. Если заглянуть в блокчейн Bitcoin, то увидите полный граф транзакций. Вы увидите, кем, кому и сколько было отправлено. Таким образом, это идеальная монета с точки зрения отслеживания.

Mimblewimble гораздо приватней. Он обеспечивает то, что я называю "годной" приватностью. Да, такой вот очень технический термин. И причина, по которой я так говорю, заключается в том, что если вы, воспользовавшись блокчейн-эксплорером, заглянете в блокчейн Wimblewimble, то увидите только входы и выходы. И вы никак не сможете определить, какие входы и с какими выходами связаны. По сути, на уровне блоков это тот же Coinjoin. И это помогает замаскировать граф транзакций. И, конечно же, все значения тоже скрыты. О том, как именно это работает, я расскажу чуть позже.

Безусловно, проблема остаётся: целеустремлённый и мотивированный злоумышленник может просканировать сеть, и если он разместит в сети достаточное количество узлов, то сможет отслеживать одноранговую сеть на предмет проводимых транзакций, которые являются атомарными, и таким образом восстановить граф транзакций. То есть, приватность, обеспечиваемая Mimblewimble хороша, она нормальна, но не фантастична, и уж точно не сравнится с приватностью, которую даёт Monero.

Что хорошо в Mimblewimble, так это масштабируемость. И поэтому гарантии безопасности, или, скорее, компромиссы в области безопасности, на которые идёт Mimblewimble, сводятся к тому, что, проведя транзакцию, вы можете просто выбросить её. Вы можете больше даже не вспоминать о ней. Для того чтобы проверить состояние блокчейна, всё, что вам действительно нужно, - набор непотраченных выходов. То есть все монеты, которые находятся в обращении. Вам просто нужно знать их, а также знать кривую эмиссии. И тогда вы сможете провести независимую проверку состояния блокчейна. Придётся произвести ещё кучу других действий, но с точки зрения учёта это всё. И поэтому, если бы Bitcoin работал подобным образом, то, вероятно, можно было бы выбросить до 80% блокчейна. Так что это хорошее решение с точки зрения масштабирования, к тому же оно интерактивно.

А теперь немного математики. И если вам претит математика, то здесь имеется соответствующее предупреждение. Но, учитывая некоторые из сегодняшних выступлений, думаю, все уже готовы к этому. Но даже если вы знаете математику только на уровне средней школы, вы всё поймёте. Я постарался сделать объяснение как можно более доступным.

Давайте начнём с того, как работают конфиденциальные транзакции. Ключевая проблема здесь заключается в том, как узел принимает транзакцию через блокчейн или в сети - он должен при этом знать, что при этом ничего не создаётся и не тратится не надлежащим образом. Также при этом он не должен знать фактической суммы, о которой идёт речь. Похоже на чёрную магию, не так ли? И сейчас я расскажу, как это делается.

Итак, давайте рассмотрим пример транзакции. У Элис есть некий выход, у неё имеется 100 Tari, и она хочет отправить их Бобу. Транзакция будет выглядеть примерно так. Она потратит этот выход, по факту этот выход должен появиться у Боба, она получит какую-то сдачу, и, конечно же, будет уплачена некая комиссия.

В таком блокчейне, как Bitcoin, где всё открыто, узлы могут вести учёт напрямую. То есть они видят транзакцию, просто сравнивают выходы и входы, проверяя, равны они или нет, так? Равна ли разница выходов и входов нулю. В данном случае значение выходов у Боба равно 10, у Элис - 89, при наличии комиссии Tari, равной единице, и при условии, что она тратит 100. Мы складываем эти значения и получаем ноль. Отлично! Никто не делает ничего плохого.

Но как это сделать, не зная значений? Сегодня вы уже несколько этот термин уже звучал здесь пару раз: обязательства Педерсена. Так что же на самом деле здесь происходит? В криптографии, которую мы используем в таких случаях, в случае с эллиптическими кривыми или ECC, применяются обычные правила арифметики. Сложение и умножение работают точно так же, как и в любой школьной задаче по алгебре. То есть вы можете взять любое число k, умножить его на некоторую константу G и получить некоторое значение P. Таким образом, k умножить на G равно P.

В случае с эллиптической кривой это сделать так же просто. Умножение - это просто, поэтому мы можем вычислить P. Но дело в том, что если я дам вам значение P, вы не сможете сказать, что P делится на G. Вы никогда не сможете вычислить k при отсутствии безумного объёма вычислительной мощности. Я говорю "никогда", но пуристы скажут, что теоретически это не так. Однако но на практике вы в принципе не сможете найти k. Поэтому все оранжевые значения являются публичными, а все белые - секретными. И вы, возможно, уже догадываетесь, что белые значения - это секретные ключи, а оранжевые - открытые. И, по сути, это криптография с открытыми и закрытыми ключами.

Итак, это первый шаг. Шаг второй - это обязательства. Далее мы делаем следующее: поскольку здесь применяются обычные правила арифметики, вы знаете старое доброе правило перемещения и ассоциативное правило, распределительное правило математики, где A плюс B равно B плюс A, или A плюс B плюс C равно A плюс B плюс C. И вы можете проделать всё те же арифметические трюки со значениями эллиптической кривой. Поэтому, когда мы создаём обязательство, мы фактически складываем два слагаемых. Мы берём одно секретное значение, умноженное на константу, и другое секретное значение, умноженное на константу, и складываем их вместе и получаем обязательство. И если у вас есть два разных обязательства, в игру вступает одно замечательное свойство: если вы сложите их вместе, то получите третье: C. Точно такой же ответ, как если бы вы сложили эти два секрета вместе и эти два значения вместе и выполнили математические действия с обязательствами, получив тот же ответ. Это называется гомоморфным свойством обязательств. И это своего рода секретный механизм Mimblewimble.

А теперь добавим этим обязательствам некоторой семантики. Итак, то, что мы имеем на выходе Mimblewimble фактически представлено вот этими обязательствами. Это сумма значений, умноженная на G. Это секретное значение является ключом траты. Зная это значение, вы сможете потратить выход. И фактическое значение выхода умножается на H. Итак, это два секретных значения обязательств Mimblewimble. Но то, что мы показываем, то, что публикуется в блокчейне, - это просто сумма. Поэтому, как только я сложу эти два значения, вы уже ничего не сможете сделать. Их уже никогда нельзя будет разделить. Это всё равно, как если бы я вам просто назвал сумму. То есть, у меня в голове были бы два каких-то числа, сумма которых бы составляла миллион. Что это за два числа? Нет реального способа выяснить, что это за два числа, не перебрав все возможные комбинации, верно? А в данном случае число таково, что сумма здесь составляет даже не миллион. Она доходит до астрономического числа. Так что практического способа вычислить эти два числа просто не существует.

На этом вводная часть закончена, и теперь давайте посмотрим, как всё то, что сделано в Tari, отличается от того, как то же самое реализовано в Bitcoin.

Итак, Элис точно так же тратит выход, отправляя его Бобу, получает сдачу и оплачивает комиссию. И поскольку в Mimblewimble всё это представлено обязательствами, мы имеем Ca и Cb, где простое число Ca является обязательством Элис по сдаче. Здесь мы имеем значение, равное 100, и ключ траты. У Боба значение 10 и ключ траты. Значение сдачи равно 89. И если мы решим подвести баланс, мы просто сложим эти обязательства. И благодаря этому правилу ассоциативности мы можем сложить все H, а также все G, и увидеть, как значения сокращаются, правильно? Точно так же, как и на этой стороне. Но на стороне G у нас есть сумма того, что фактически является суммой всех секретных ключей, всех ключей траты. И это остаток. То, что осталось.

И в чём же важность всего этого? Важность в том, что когда у вас есть сумма всех ключей и вы умножаете её на G, это похоже на открытый ключ. А когда у вас есть открытый ключ, вы можете создать цифровую подпись и подписать её секретным ключом. Итак, в Mimblewimble мы делаем так, что узел получает просто набор обязательств. Он вычисляет баланс обычным способом, а затем проверяет, является ли результат открытым ключом, соответствующим подписи, которую сторона, производящая трату, предоставила вместе с транзакцией. И если подпись подтвердится, значит, соответствующие значения были сокращены. Так можно убедиться в том, что ни одна монета не была создана или уничтожена, но при этом мы понятия не будем иметь о том, каковы были точные значения. На этом наш урок закончен.

Теперь давайте посмотрим, каковы в данном случае требуются разрешения на совершение траты? В случае с Bitcoin Элис при совершении траты должна будет предоставлять скрипт траты для своего выхода, скрипт блокировки для сдачи, и выход Боба, в то время как Боб фактически не предоставляет ничего. Интерактивность отсутствует полностью - Элис всё отправляет сама.

В Tari Элис демонстрирует знание ka и va, выход, который она тратит, она создаёт секрет для сдачи, но она не может создать секрет для выхода Боба. Если бы она это сделала, то смогла бы потратить его выход, верно? Поэтому Бобу нужно войти в историю и предоставить свой секрет, своё значение kb. Вот почему Mimblewimble интерактивен. И это усложняет например, получение чаевых, например, вывод средств с бирж и из майнинговых пулов - едва ли майнинг-пул будет ждать, пока все войдут в сеть, чтобы выплатить дивиденды и так далее. И это требующая решения проблема Tari. Нам также хотелось бы реализовать целый ряд вещей между первым и вторым уровнем Tari, например, привязку к сайдчейну или ко второму уровню, реализовать ковенанты и прочие вещи для управления нашими смарт-контрактами.

И вернёмся на шаг назад. Мы можем подвести итог. Унифицированные транзакции Mimblewimble конфиденциальны, то есть, интерактивны. И ещё одно: всё сводится к простой математике. Здесь нет ничего сложного. Это не похоже на Bitcoin, где приходится использовать скрипты. Некоторые из вас, возможно, не знают, что когда вы проводите транзакцию на адрес Bitcoin, то никакого реального адреса просто нет. Транзакция отправляется не на адрес. Есть скрипт, который проверяется, скрипт разблокировки должен соответствовать подписям и так далее. Но в случае с Mimblewimble, по сути, это просто подпись, просто математика.

Но как нам реализовать атомарные свопы, привязки к сайдчейну, односторонние платежи, ключи просмотра, ковенанты, время хэширования, контракты блокировки и прочие глупости вроде BRC-20? Дело в том, что в унифицированные транзакции Wimblemimble не позволяют этого сделать, и поэтому вводим TariScript. Прошло 15 минут, и мы наконец-то добрались до сути разговора.

И как мы это собираемся сделать? Всё сводится к двум вещам. Мы изменяем одно правило консенсуса и добавляем ещё одно. Итак, первое, что мы сделали, мы изменили правило траты выходов Tari: чтобы потратить выход Tari, необходимо знать две вещи: ключ траты, что является уже существующим правилом Mimblewimble - вам нужно знать значение k, но теперь вам также нужно знать нечто названное нами скрипт-ключом, и это дополнительное правило.

Также есть новое правило консенсуса, согласно которому, когда вы создаёте выход или когда вы должны предоставить скрипт с этим выходом, когда вы тратите его, вы можете добавить некоторый вход. Вы можете добавить к скрипту любой вход по вашему выбору, но скрипт должен выполняться узлом правильно согласно правилам консенсуса, и в результате должно получиться одно значение, и это значение должно быть открытым ключом. А затем сторона, совершающая трату, должна доказать знание закрытого ключа, соответствующего такому открытому ключу. Этот закрытый ключ мы и называем скрипт-ключом.

Как мы реализуем это в Tari? Вдохновившись Bitcoin Script, мы придумали нечто под названием TariScript. Это стековый язык, очень похожий на Forth или Bitcoin Script. Он не обладает свойством полноты по Тьюрингу, поэтому в нем нет циклов. Но в нём есть опкоды для выполнения обычных математических операций. Вы можете создавать подписи, производить хэширование. Вы можете включить некоторые метаданные, например, высоту блока. В нём присутствуют условные операторы, так что вы можете использовать условную логику. Таким образом, это своего лёгкий вариант смарт-контракта. У него есть строгие ограничения, налагаемые правилами консенсуса, определённый размер и сложность, и поэтому нет проблем с прерываниями - каждый сценарий будет гарантированно завершён.

Рассмотрим несколько примеров. Самый простой - как выглядит стандартная транзакция Mimiblewimble, стандартная интерактивная транзакция Tari? В этом случае скрипт самый простой. Настолько, насколько можно придумать, это no-op - он ничего не делает. Поэтому, когда пользователь совершает трату, в качестве входа берётся любой открытый ключ. Скрипт no-op выполняется с сохранением этого ключа в стеке, что соответствует правилу. При выполнении скрипта в стеке остаётся один открытый ключ. И если пользователь не полный идиот, он будет знать закрытый ключ, соответствующий открытому ключу, который он только что включил. При этом предполагается, что согласно новым правилам консенсуса ключ траты также будет известен. Так что это, опять же, требует интерактивности и не противоречит стандартной унифицированной версии.

На мой взгляд, более интересным предметом являются односторонние платежи, когда Элис может отправить что-то Бобу, и Боб в этом не будет принимать никакого участия, как в случае с транзакциями Bitcoin, например, или Monero. в рамках данного сценария Элис, скрипт помещает открытый ключ Боба в стек, и когда Боб совершает трату, он не предоставляет никаких данных. Таким образом, транзакция будет выполнена, а в стеке останется только открытый ключ Боба. С этой частью мы разобрались. Но что насчёт ключа траты?

Когда Элис создаёт эту транзакцию, она создаёт общий секрет между ней и Бобом, используя механизм, называемый обменом ключами Диффи-Хеллмана. Это стандартная техника, воспользовавшись которой, две стороны создают общий секрет, и никто из наблюдателей не может понять, что это за секрет. Но эти две стороны знают его - это общий секрет.

В обычной версии Mimblewimble это не сработает, поскольку после того, как Элис отправит транзакцию в сеть, она сразу узнает этот секрет и сможет потратить выход Боба. Далеко не идеальный вариант. Однако теперь, с TariScript, она не сможет узнать закрытый ключ из открытого ключа Боба. Таким образом, из них двоих теперь только Боб сможет потратить монету, и на примере Боба мы получаем те самые односторонние платежи.

А можно реализовать ещё более интересные вещи. Например, Элизабет чуть раньше рассказывала об атомарных свопах, требующих условий для возврата и тому подобные вещи. Данный скрипт будет определять, что, например, до блока 4000 в стек может быть помещён только открытый ключ Боба. Но после блока 4000 в стеке останется либо открытый ключ Элис, либо открытый ключ Боба. И оба они смогут его потратить. Таким образом, до блока 4000 только Боб сможет произвести трату. После 4000 трату сможет произвести либо Элис, либо Боб. Таким образом, в случае неудачного атомарного свопа она сможет вернуть свои средства.

В общем, это был своеобразный такой ускоренный просмотр TariScript. Я опустил множество деталей. Чтобы узнать подробности, следует ознакомиться с документом. Я опустил то, что основная идея TariScript в том виде, в котором я представил её здесь, была придумана мной за пару дней, начальная спецификация была составлена за неделю или около того, но нам потребовалось больше года, чтобы довести протокол до ума и сделать его безопасным.

И из-за того, что я всё представил кратко, возможно, чтобы разобраться во всём, вы спросите меня о сквозной отправке и о том, как это соотносится с самой идеей TariScript, как нам удалось решить эти проблемы и исправить их. А когда я расскажу, вы, вероятно, захотите спросить меня о том, что такое горизонтальная атака и как они могут отразиться на подходе TariScript, и что мы в Tari делаем, чтобы справиться с этим. Но, чтобы сэкономить время, мы можем обсудить это за кружкой пива.

В конечном счёте, как я уже сказал, всё это заняло большую часть года. Командой была проделана невероятная работа. И я хочу поблагодарить всю команду ведущих разработчиков Tari за то, что они учитывали комментарии и предложения, находили уязвимости, вносили исправления, находили очередную уязвимость, снова и снова проходили через итерации, и каждый раз становились чуть ближе к цели. Также хочу сказать спасибо Дэвиду Беркетту, который столкнулся с аналогичными проблемами, когда пытался реализовать односторонние платежи для блоков расширения Litecoin. Мы в долгу перед ним. Он также внёс большой вклад. И я считаю, что это просто чудесно, что мы работаем в индустрии, где люди из якобы конкурирующих проектов могут работать вместе над решением общих проблем - кажется, мы больше заняты решением технических проблем, а не пытаемся победить в каком-то неофициальном соревновании. Так что спасибо этим ребятам. На этом всё. Предлагаю вдарить по пивку.