---
title: "Цифровой отпечаток флуда: криминалистический статистический анализ аномального роста объёма транзакций Monero в середине 2021"
date: "2021-09-21"
categories:
  - "Статьи"
tags:
  - "Исследования"
thumbnail: "img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/01.png"  
lead: "Разбор аномального роста объёма транзакций в сети Monero во второй половине июля 2021 года"
pager: true
toc: true
sidebar: "right"
---

**Контрибьюторы**: [Isthmus](https://github.com/mitchellpkt/) (Митчелл П. Кравиц-Тейер), [Neptune](https://github.com/neptuneresearch), [Rucknium](https://github.com/rucknium), [Jberman](https://github.com/j-berman), [Carrington](https://github.com/carrington1859)
**Контактная информация**: [isthmus@getmonero.org](mailto:isthmus@getmonero.org)
**Код**: см. [репозиторий проекта](https://github.com/noncesense-research-lab/xmr_volume_anomaly) и [заметки по визуализации](https://github.com/noncesense-research-lab/xmr_volume_anomaly/blob/main/analysis_profile_v1.ipynb)

## _Введение_

Во второй половине июля 2021 года в сети Monero произошёл аномальный рост объёма транзакций. На данном графике ежедневного объёма транзакций он обозначен красной линией:

![02](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/02.png)

Этот неожиданный взлёт не мог не вызвать удивления, а на ум естественным образом приходило лишь несколько вопросов в отношении «источника» избыточного объёма транзакций:
- Является ли источником сразу множество лиц?
- Каков цифровой отпечаток программного обеспечения и поведенческие сигнатуры у аномальных транзакций?
- Сколько транзакций было сгенерировано источником, и сколько на это было им потрачено?

К счастью, у нас имеются данные, чтобы попытаться ответить на эти вопросы в отношении аномалии и её источника. Данные нами были взяты у Neptune и из базы данных [Noncesense Research Lab](https://noncesense-research-lab.github.io/).

Если вы хотите перейти непосредственно к ответам, то можно перескочить непосредственно в раздел «Выводы». Если же вам хотелось бы погрузиться глубже в суть вопроса и узнать, как именно нами проводился анализ проблемы, то все мельчайшие подробности приводятся ниже. Следует отметить, что данная статья рассчитана на читателя, знакомого с концепцией кольцевых подписей и механизмом обеспечения приватности. Соответствующую информацию можно найти в третьей главе [Овладевая Monero](http://www.masteringmonero.com/), работы, которая, благодаря щедрому финансированию со стороны сообщества, находится в свободном доступе.

## _Принципы и ограничения, связанные с анализом_

Перед тем как двигаться дальше, предлагаем обсудить фундаментальную идею, лежащую в основе этого анализа (и ограничения, связанные с ним). Последующий анализ не подразумевает деанонимизации произвольно отобранных отдельных транзакций и статистически осуществим только в случае с кошельками с большим объёмом проводимых транзакций (от сотен до тысяч транзакций в день). Другими словами, такое совокупное профилирование не должно волновать обычных пользователей. Для прояснения ограничений в этом разделе приводится нетехническая аналогия ключевой концепции, лежащей в основе этого совокупного анализа.

Как удалось произвести профилирование аномалии, не отслеживая отдельные транзакции? Нами рассматривалась общая статистика и то, как она изменялась с ростом количества транзакций. В качестве аналогии возьмём фруктовый лоток, на котором каждое утро обычно имеется примерно десяток различных видов фруктов: бананов, лаймов, яблок и апельсинов. В большинстве дней лоток выглядит вот так:

![03](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/03.png)

Однажды утром вы видите, что фруктов в ДВА РАЗА больше, чем обычно! Когда никто не смотрел, какой-то продавец вывалил на витрину лишнюю коробку с фруктами. Простое знание того, что фруктов в два раза больше, не позволяет вам сказать, что «это было добавлено мистическим способом. Но это не значит, что мы не можем сделать никаких выводов для себя. Вот как это выглядит сейчас:

![04](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/04.png)

Вероятно, сейчас у вас возникло обоснованное предположение: если вместо обычных 25% лотка сейчас 65% занято яблоками, то, вероятно, источником этих «лишних» процентов является поставщик яблок. Поскольку сегодня вместо 4 (или около того) обычных яблок сегодня на лотке аж 18, можно произвести примерную оценку, согласно которой яблок стало больше примерно на дюжину.

Статистический анализ, используемый ниже, имеет ту же логику! Мы смотрим на происходящее в блокчейне в целом во время аномального роста объёма транзакций и сравниваем преобладание различных характеристик транзакций с течением времени, что позволяет нам прийти к общим выводам.

## _Разложение объёма транзакций_

Для исходного временного ряда объёма транзакций характерны частые изменения, происходящие на ежедневной основе:

![05](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/05.png)

Причина такого точного разделения показателей на графике состоит в недельной периодичности объёма транзакций Monero:

![06](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/06.png)

Поскольку такая недельная периодичность не связана с исследуемым нами феноменом, проще взглянуть на тенденции изменения объёма, минуя такую «сезонность»:

![07](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/07.png)

## _Как установить определяющие признаки источника_

Чтобы понять, как эти графики могут быть использованы в целях выделения характеристик источника, давайте начнём с контрольного примера и возьмём транзакции с 11 выходами.

![08](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/08.png)

![09](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/09.png)

Ни наблюдаемые цифры (чёрная линия выше), ни лежащая в основе тенденция (зелёная линия выше), по сути, не изменились относительно красной линии, когда начался аномальный рост объёма. А теперь посмотрим на поднабор транзакций (кол-во выходов = 11) и зададимся вопросом: какая часть транзакций, совершённых в этот день, обладает такой характеристикой?

![10](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/10.png)

Поскольку частота проводимых транзакций с 11 выходами не выросла во время аномалии, их доля в ежедневном объёме транзакций снижается относительно красной линии. Это снижение в относительном преобладании с началом аномалии (красная линия) — это антипаттерн, означающий, что наличие 11 выходов НЕ ЯВЛЯЕТСЯ цифровым отпечатком источника.

А теперь давайте сравним эти результаты со статистикой поднабора транзакций с 2 выходами (2OTX):

![11](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/11.png)

![12](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/12.png)

![13](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/13.png)

Выше мы видим, что тенденция проведения транзакций 2OTX возрастает синхронно с аномальным ростом объёма транзакций и преобладает более чем обычно. Таким образом, мы можем отметить, что характеристика, предполагающая наличие 2 выходов, является определяющим признаком аномальных транзакций.

**_Вопрос 1(a): цифровой отпечаток источника — количество выходов_**

Мы применим использованную выше логику к первым возможным количествам выходов ниже. Повышение количества транзакций с 2 выходами (верхняя линия) очевидно.

![14](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/14.png)

Основываясь на повышении или снижении преобладания в начале аномалии (красная линия на рисунках ниже), мы можем сказать, что N=2 соответствует источнику, в то время как N=3 и N=4 являются сильным антипаттерном источника.

![15](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/15.png)

![16](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/16.png)

![17](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/17.png)

Эта тенденция характерна и для транзакций с большим количеством выходов. Как отмечалось выше, мы можем прийти к выводу, что наличие 2 выходов является цифровым отпечатком источника. Это типичное количество для большинства транзакций, включающих в себя выход получателя и выход сдачи. Следует отметить, что из-за [проблем с приватностью, возникших из-за транзакций 1TXO](https://github.com/monero-project/monero/issues/5399), теперь протокол требует, чтобы все транзакции включали в себя по крайней мере два выхода.

**_Вопрос 1(b): цифровой отпечаток источника — комиссии_**

Поскольку комиссии неоднозначны, гораздо проще бегло взглянуть на тепловую карту (ниже) и увидеть, что повышению объёма транзакций идеально соответствует существующая тенденция следования рекомендациям, которые предлагаются основным кошельком в отношении комиссий.

![18](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/18.png)

**_Вопрос 1(c): цифровой отпечаток источника — поле unlock_time_**

И снова мы видим, что источник транзакций совпадает с цифровым отпечатком основного кошелька, поскольку значение поля времени разблокировки unlock_time установлено как 0.

![19](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/19.png)

**_Вопрос 1(d): цифровой отпечаток источника — поле tx_extra_**

В поле extra каждой из транзакций, отправленных источником, содержался публичный ключ транзакции и зашифрованный идентификатор платежа (что соответствует тому, как исходный вариант кошелька строит транзакции). В совокупности это составляет 44 байта, и мы можем видеть, что количество транзакций с такой характеристикой растёт вместе с аномалией:

![20](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/20.png)

*Обновление: в более ранней версии этой статьи рассматривался вопрос: может ли наличие или отсутствие дополнительных ключей в поле tx_extra привести к утечке информации, является ли адрес получателя транзакции первичным адресом или подадресом? После редакции Koe указал на то, что такой анализ срабатывает в случае с транзакциями с 3 выходами и больше (где отсутствие дополнительных ключей окончательно указывает на то, что никаких подадресов не использовалось).*

**_Вопрос 1(e): цифровой отпечаток источника — выводы_**

Принимая во внимание статистические корреляции, можно отметить, что транзакции злоумышленника обладали следующими пятью характеристиками:
- наличие нулевого значения поля unlock_time;
- наличие публичного ключа и зашифрованного идентификатора платежа в поле tx_extra;
- расчёт комиссий в соответствии с основным вариантом реализации кошелька;
- наличие ровно двух выходов.

Все эти свойства идеально соответствуют основному кошельку, поэтому, вполне вероятно, аномальные транзакции генерировались с помощь программного обеспечения исходного варианта кошелька. При наличии такого фильтра мы можем выяснить, какая часть транзакций соответствует общему профилю.

![21](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/21.png)

**_Вопрос 2(a): Источник — это одно или несколько лиц? Анализ количества входов_**

Естественным образом возникает вопрос: стал ли аномальный рост объёма транзакций результатом действий одной стороны (например, университетской исследовательской группы, занимающейся сбором данных для написания статьи) или множества независимых лиц (например, вследствие органичного прироста пользователей в результате роста популярности платформы). Одним из способов узнать это является изучение шаблонов потребления входов (количество, время и так далее).

Для начала давайте взглянем на количество входов транзакции, которое является динамическим в зависимости от суммы транзакции и распределения суммы транзакции в кошельке. Итак, если аномалия возникла в результате органичного роста количества никак не связанных между собой лиц, можно смело ожидать, что какая-либо связь между суммами в выходах в их кошельках и влияние на количество входов будут отсутствовать. Тем не менее мы видим совсем противоположное: заметный и резкий рост количества транзакций с 1-2 входами (две верхние линии).

![22](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/22.png)

Прежде всего, можно отметить, что с началом аномалии наблюдается значительный скачок количества транзакций 1INTX и 2INTX при отсутствии заметного роста количества транзакций с тремя входами и более. Если посмотреть на боле ранние части временных рядов, то можно отметить отсутствие такого необычного шаблона до начала аномалии. Это проще увидеть, если нормализовать каждый показатель до нулевого среднего (чтобы избавиться от вертикальных смещений) и стандартного отклонения от единицы (чтобы привести их к одному масштабу).

![23](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/23.png)

Если взглянуть на данные за 2021 год выше, можно выделить четыре различные фазы. В Фазе A, где наблюдается взлёт или спад объёма транзакций, это всегда отражается на количестве входов. Это именно то, что мы ожидаем при органичном использовании. В Фазе B имеются взаимосвязанные транзакции с 4 и большим количеством входов, что никак не отражается на количестве транзакций с 1-2 входами. Эту странность мы не станем подробнее разбирать в этой статье. В Фазе C ничего особенного не происходит. Но затем, во время аномалии в Фазе D, наблюдается беспрецедентное поведение, которое в значительной мере можно противопоставить тому, что происходит в Фазе B, а именно, невероятный (стандартное отклонение от 4) скачок количества транзакций с 1-2 входами, который никак не отражается на количестве транзакций с четырьмя входами и больше.

Чтобы получше разобраться в ситуации, давайте возьмём небольшое количество (скажем, 2 входа) и одно большое (скажем, 4 входа) и сравним их абсолютные значения. Если взглянуть на Фазы A-C, то можно вообразить, что они относительно взаимосвязаны, и, действительно, мы видим, что в данных за год (YTD), а это одна точка за день, почти весь набор данных попадает в конус нормальности и лишь единожды сильно выходит за пределы типичного диапазона.

![24](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/24.png)

Как, вероятно, вы догадались, предельное отклонение соответствует аномалии, обозначенной здесь обведёнными точками данных:

![25](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/25.png)

Если поместить график корреляции количества входов рядом с временными рядами количества входов Фазы D, то можно увидеть две подфазы, a и b:

![26](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/26.png)

В первой части (a) временные ряды (слева) демонстрируют солидный рост количества транзакций с 1-2 входами, что не сопровождается типичным связанным с этим ростом количества транзакций с 4 входами и более. Это продемонстрировано на графике взаимосвязи (справа) горизонтальным основанием беспрецедентного отклонения от конуса нормальности. Во второй части (b) по мере развития аномалии и сокращения объёма количество транзакций с 1-2 входами начинает откатываться вниз, в то время как количество транзакций с 4 входа ми и более повышается на два стандартных отклонения и в конечном счёте возвращается обратно в конус нормальности.

Зачем мы всё это так внимательно и подробно рассматриваем? Давайте вернёмся к сценарию органичного роста: опираясь на интуицию и исторические данные, мы ожидаем, что резкий рост объёма транзакций отразится на значениях количества входов, остающихся в конусе нормальности. Но что мы видим вместо этого? Рост объёма транзакций, при котором практически все транзакции содержат 1-2 входа и имеют характеристики далеко за пределами исторической нормы.

Это интересно, поскольку основной кошелёк предпочитает создавать транзакции с 1-2 входами до того, как перейдёт к транзакциям с 3 входами и больше. Проведём мысленный эксперимент и представим, что у нас имеется отдельный кошелёк с большим количеством доступных выходов, которые можно потратить (mise en place, так сказать). Что случится, если мы сегодня активируем переключатель и начнём генерировать кошельком огромное количество транзакций с маленькими суммами, которые он будет передавать самому себе? Первые несколько дней у кошелька будет большой выбор существующих выходов, и в целом он будет в состоянии достичь своей цели, создавая транзакции с 1-2 входами (с незначительным количеством транзакций с 3 и более входами). Тем не менее с течением времени выходы будут создаваться и уничтожаться, и в конечном счёте кошелёк станет более ограниченным в выборе, и ему придётся перейти к более частому созданию транзакций с 3 и более выходами. Почему выбор станет более ограниченным? Потому что наш стандартный кошелёк производит только транзакции с 2 выходами: выход для себя как получателя и выход сдачи. Таким образом, если у нам имеется 500 доступных выходов, а затем мы строим транзакцию, в которой тратится 5 выходов и создаётся 2 выхода, то у нас остаётся уже 497 выходов. Фактически любая транзакция с 2 выходами и 3 или большим количеством входов будет сокращать количество непотраченных выходов кошелька и таким образом ещё больше сокращать последующий выбор входов.

**_Вопрос 2(b): Источник — это одно или несколько лиц? Анализ распределения времени траты_**

Продолжим начатый выше мысленный эксперимент. Если у нас имеется кошелёк со множеством доступных выходов, а затем мы активируем переключатель, в результате чего кошелёк начинает очень быстро отправлять транзакции самому себе, как это всё повлияет на распределение участников кольца по времени их создания? Изначально, поскольку новые выходы ещё не были созданы, кошелёк будет строить транзакции, использующие выходы, которые появились до того, как переключатель был активирован. Поэтому мы не увидим значительных изменений с точки зрения частоты выбора более «молодых» участников кольца. Но с течением времени старые выходы будут потрачены, и кошельку в силу необходимости придётся строить транзакции из более поздних выходов, которые были созданы уже после активации переключателя.

Давайте вернёмся от мысленного эксперимента к реальным данным блокчейна и посмотрим на «возраст» каждого участника кольца в каждой отдельно взятой транзакции, сгенерированной за последние несколько месяцев, а на этой основе создадим тепловую карту.

![27](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/27.png)

Этот график может рассказать нам о многом, но сегодня сфокусируемся на том, что связано с появлением аномальных объёмов транзакций. Увеличим правый нижний угол графика и взглянем на обведённую кругом особенность:

![28](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/28.png)

Недели наблюдений вплоть до появления аномалии (левая часть чёрной пунктирной линии) приблизительно соответствуют ожиданиям в отношении того, насколько часто кошелёк будет выбирать ложные выходы из транзакций, созданных менее 50 блоков назад: иногда, но не часто. С момента начала аномального роста сперва происходит незначительное изменение частоты включения выходов, созданных менее 15 блоков назад, в транзакции, предположительно потому, что сначала тратятся более старые выходы. Но вскоре наблюдаемая тенденция стремительно смещается, и уже непропорционально большое количество участников кольца представлены выходами, появившимися в течение последних 15 блоков, что ожидаемо в том случае, если набор старых выходов потрачен, в результате чего кошелёк вынужден использовать выходы, созданные при проведении транзакций во время аномалии.

Этот эффект также наблюдается, если посмотреть на возраст самого молодого участника кольца, который при нормальных условиях, как правило, составляет в среднем 40 блоков. С началом аномального роста объёма транзакций этот возраст резко смещается в сторону более поздних блоков, что предполагает использование совсем недавно созданных выходов.

![29](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/29.png)

**_Вопрос 3: Сколько транзакций было создано, и каковы были соответствующие затраты?_**

Этот раздел будет ОЧЕНЬ теоретическим и будет содержать целый ряд допусков, которые могут стать причиной значительной ошибки. Отнеситесь к этой оценке со здоровой долей скептицизма. Сначала давайте рассмотрим аномалию и непосредственно предшествующую ей базовую линию:

![30](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/30.png)

Если допустить, что базовый органичный объём остался тем же, то мы можем убрать смещение и оценить исходный объём:

![31](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/31.png)

Объединение с приведённой выше кривой количества транзакций (по правую сторону от красной линии) даёт нам оценку количества транзакций «сверх» нормы: 365 000 транзакций в течение нескольких недель. Аномальный объём транзакций проводился со стандартными комиссиями, что на тот момент при такой конструкции составляло 0,000015 XMR за транзакцию. Таким образом, мы можем оценить и ежедневные затраты на их создание:

![32](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/32.png)

Применив общую сумму к этому окну, мы получаем оценку общих затрат, составляющую 5 XMR:

![33](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/33.png)

На тот момент обменный курс Monero составлял примерно 200 USD за XMR. Таким образом, затраты на создание приблизительно 365 000 транзакций составили 1000 USD. Транзакция, содержащая 2 входа и 2 выхода, весит примерно 1,93 Кбайт, а значит, эти транзакции увеличили размер блокчейна приблизительно на 700 Мб при затратах 1,40 USD на Мб.

## _Выводы_

Давайте вернёмся к вопросам, заданным в начале, но уже опираясь на то, что мы наблюдали выше.

**Является ли источником одно или сразу множество лиц?** Всё указывает на то, что это было одно лицо. Несмотря на то, что гомогенность транзакций является сильным признаком, шаблоны потребления входов всё же позволяют прийти к более обоснованным выводам. В случае органичного роста в результате появления новых независимых лиц, как правило, можно ожидать наличия «полусогласованных» тенденций для различного количества входов и полного отсутствия согласованности между кошельками независимых пользователей. Во время аномального роста мы вместо этого наблюдали крайне нетипичный всплеск количества транзакций с 1-2 входами при отсутствии незначительного повышения количества транзакций с 4 входами и более.

**Каков цифровой отпечаток программного обеспечения и поведенческие сигнатуры у аномальных транзакций?** Кажется, аномальные транзакции были сгенерированы основным кошельком или же каким-то другим кошельком, соответствующим его сигнатуре. Источник использовал те настройки комиссий и времени разблокировки, которые используются по умолчанию, и генерировал исключительно транзакции с двумя выходами. Транзакции генерировались как можно быстрее, что привело к частой трате выходов, появившихся всего в течение 10-15 последних блоков.

**Сколько транзакций было сгенерировано источником и сколько на это было им потрачено?** По очень грубой оценке было создано 365 000 транзакций при общих затратах, составивших 5 XMR (на тот момент примерно 1000 USD). По расчётам, сделанным на салфетке, можно предположить, что аномальные транзакции увеличили размер блокчейна примерно на 700 Мб при затратах 1,40 USD за один Мб.

## _Будущая работа_

До настоящего момента мы по большей части фокусировали наше внимание на совокупной статистике и количественных показателях и даже не касались «генетического» анализа. Из-за масштабов и скорости аномалии, вероятно, многие кольца можно будет деанонимизировать (то есть мы сможем идентифицировать, какие из выходов были действительно потрачены, а какие являются ложными). У нас уже есть зацепка в виде цифрового отпечатка аномалии, которая позволяет нам исключить участников (в соответствующих сигнатурах). В данном контексте участников колец из только что преобразованных coinbase-транзакций также можно исключить. Факт того, что создание транзакций было таким быстрым (см. раздел 2b), также является губительным с точки зрения приватности аномальных транзакций. Поскольку большое количество транзакций было сгенерировано с крайне коротким временем траты (выходы, как правило, использовались в течение 10-15 блоков после создания), вероятно, [эвристический подход с поиском самого последнего](https://arxiv.org/pdf/1704.04299/) будет весьма эффективным.

Более того, топологический анализ дерева транзакций, вероятно, окажется очень информативным. Мы предположили, что средства обычно распределяются между лицами и счетами. В обычных случаях выходы транзакций отправляются различным получателям (например, 1 выход — в кафе, 1 — обратно в кошелёк в качестве сдачи). Однако в случае, когда основной кошелёк многократно осуществляет передачу самому себе, выход, предназначенный для получателя, и выход сдачи уходят одному в один и тот же кошелёк и могут быть объединены позднее!

Если аномалия не демонстрировала чрезвычайно точных методов управления изменениями, вполне вероятно, что во многих случаях два выхода, созданные в результате проведения конкретной транзакции, будут использованы одной и той же или последующими транзакциями. Рекомбинация параметров в графике обозначает топологическую сигнатуру, которая будет проявляться довольно часто в случае так называемого «вспенивания», если сравнивать со случаями случайного выбора ложных выходов. Основной кошелек алгоритмически пытается распределить выборку входов, чтобы избежать возникновения очевидных рекомбинаций (например, использования двух выходов одной и той же транзакции в качестве входов другой транзакции). Таким образом, рекомбинации не будут очевидными при просмотре блокчейн-эксплорера, однако анализ топологии графов может идентифицировать эти циклы, даже если рекомбинации будут распределены в нескольких попытках проведения по разным узлам и в течение нескольких часов или дней.

В случае с мысленным экспериментом, чтобы продемонстрировать, почему происходит именно так, представьте следующий сценарий:

```
# Run indefinitely until the wallet runs out of funds
while 1==1:
    try:
        core_wallet.transfer(amount=1, recipient=self.address)
```

Единственный способ опустошить кошелёк — потратить все имеющие ценность входы, которые вы создали во время аномального роста. Учитывая свойство конвергенции, о котором говорилось в самом конце раздела 2(а), мы понимаем, что все первые 100 000 выходов, созданных во время аномалии, находятся в верхней части дерева транзакций, начиная со 100 последних аномальных транзакций. Единственный способ объединения 100 000 выходов в 100 выходов состоит в постоянном создании комбинаций.

Учитывая все эти факторы, вполне вероятно, что во многих случаях истинные траты можно будет эвристически вычислить в случае с аномальными транзакциями. Вспомните аналогию с фруктовым лотком — это более чем вполне возможно из-за аномальной однородности и явного увеличения объёма, если сравнивать с исходным уровнем, и не настолько применимо к обычным пользователям, обеспечивающим довольно небольшой объём транзакций. Одним из интересных полей дальнейшего исследования может стать частота использования транзакций, соответствующих аномальной сигнатуре, в кольцах транзакций, не соответствующих аномальной сигнатуре, что позволит установить верхнюю границу потенциального влияния аномалии на обычные транзакции при выборе ложных выходов. Основываясь на предполагаемом объёме транзакций от источника, о котором говорилось в разделе, посвящённом оценке количества транзакций и соответствующих затрат, даже на пике избыточного объёма мы можем говорить о том, что менее половины транзакций принадлежит аномальному периоду (17 500 из 40 000 в самый показательный в этом плане день).

Между прочим, за несколько месяцев до основного аномального периода, исследуемого в этой статье, уже появлялась похожая сигнатура распределения участников кольца по «возрасту» (и некоторые другие признаки). Несмотря на отсутствие окончательной связи, всё происходившее выглядит довольно соответствующе описанному, и проявившаяся раннее аномалия также возникла во время аномально высокого роста объёма транзакций.

![34](/img/copyright/articles/2021-09-21-fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021/34.png)

---

_Источник: [Fingerprinting a flood: forensic statistical analysis of the mid-2021 Monero transaction volume anomaly](https://mitchellpkt.medium.com/fingerprinting-a-flood-forensic-statistical-analysis-of-the-mid-2021-monero-transaction-volume-a19cbf41ce60)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_