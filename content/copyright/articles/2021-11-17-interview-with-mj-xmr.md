---
title: "Над чем работает MJ-XMR. Руководство для дилетантов"
date: "2021-11-17"
categories:
  - "Статьи"
tags:
  - ""
lead: "Как страстный сторонний наблюдатель я стараюсь понять, чем занимаются разные разработчики. Однако, даже несмотря на то, что MJ пишет очень подробные отчёты по своей работе, я изо всех сил пытался понять, в чём же заключается суть его работы. Если вы ощущаете нечто похожее, то эта статья для вас."
pager: true
toc: false
sidebar: "right"
---

[mj-xmr](https://github.com/mj-xmr) является разработчиком Monero, приступившим к работе над проектом в мае 2020 года. С тех пор было профинансировано 3 его рабочих предложения в CCS, и [последнее](https://ccs.getmonero.org/proposals/mj-part-time-2021-q4.html) было полностью профинансировано буквально только что.

Читая эти отчёты, я чувствовал себя человеком, который впервые видит футболку, показанную ниже, но не знает, как работает система счисления base-2. Я мог прочитать весь текст, но он не имел для меня никакого смысла!

![01](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/01.jpg)

Обычно довольно легко понять, чем занимаются разработчики и исследователи. Например:

![02](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/02.jpg)
- **Говард Чу** — создатель программной библиотеки Lightning Memory-Mapped Database (LMDB), которая используется для хранения и обслуживания блокчейна Monero. Совсем недавно в тесном сотрудничестве с разработчиком [Tevador](https://github.com/tevador) он принял участие в создании протокола майнинга Monero, устойчивого к использованию ASIC, под названием RandomX.

![03](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/03.jpg)
- **Саранг Ноезер** — член Исследовательской лаборатории Monero, сыгравший ключевую роль в реализации таких криптографических механизмов, как Bulletproofs, DLSAG и Dandelion++.

![04](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/04.png)
- **Moneromooo** — анонимный, но плодовитый разработчик C++, который, безусловно, [написал самый активно используемый](https://github.com/monero-project/monero/graphs/contributors) в проекте Monero код.

Если позаимствовать аналогию с американским футболом, к которой прибегнул [Redditor](https://www.reddit.com/r/Monero/comments/m4764j/comment/gqtd7fu/?utm_source=share&utm_medium=web2x&context=3), упомянутые выше ребята похожи на принимающих и задних бегущих команды, то есть именно они забивают голы и становятся знаменитыми. Используя эту аналогию, можно сказать, что есть и менее известные разработчики, подобные лайнменам нападения, которые не удостаиваются такой славы и известности, но всё же играют важную роль.

Итак, после некоторого обмена сообщениями в IRC MJ согласился на телефонный разговор, чтобы обсудить то, чем он занимается. Эта статья является попыткой объяснить дилетантским языком, над чем он работает!

## _Прошлая работа MJ-XMR_

MJ в основном работал над *оптимизацией инструментов, которые разработчики используют для модификации и построения проекта*.

Что это означает? Объяснение будет, скорее, иметь отношение к разряду метазнаний.

Чтобы разобраться в этом, давайте сперва вернёмся на шаг назад и посмотрим, как строится программное обеспечение Monero. В данном случае есть несколько различных этапов:
1. Чтобы люди в глобальном смысле сотрудничали, работая над Monero, мы/они используем протокол под названием Git, а также основанный на нём сервис под названием GitHub.
2. Если пользователь хочет внести вклад, он копирует исходный код на свой компьютер, а затем вносит в него соответствующие изменения.
3. Как только изменение будет внесено, пользователь должен скомпилировать исходный код в выполняемый файл и провести тестирование, чтобы определить, работает ли тот надлежащим образом.
4. Если файл работает, изменения загружаются на GitHub, сопровождаемые запросом об их включении в основную ветку (это называется пул-реквестом или PR).
5. Наконец, пул-реквест проходит тест на непрерывную интеграцию (CI), чтобы проверить, не нарушает ли он изменение каких-либо критических параметров.

Из всего перечисленного MJ уделял основное внимание этапу компиляции и оптимизации этапа непрерывной интеграции.

Почему это важно? Давайте в качестве примера рассмотрим компиляцию. Последствия медленной компиляции могут быть следующими:
1. Разработчики зачастую избегают компиляции и тестирования. Вместо этого они могут ждать до тех пор, пока не накопится целый ряд изменений. И это является проблемой, поскольку в случае возникновения ошибки придётся выяснять, какое из множества изменений её вызвало.
2. Длительные задержки влияют на процесс разработки в целом. Если перед тем, как протестировать ваше изменение, вам придётся длительное время ожидать компиляции, вас легко могут отвлечь совершенно другие вещи, в результате чего количество продуктивных часов в течение дня сократится.

Хотя известные разработчики прекрасно знают, какие тесты проводить с каким изменением (что позволяет не проводить всех тестов), временами им приходится проводить полную рекомпиляцию, а значит, это напрямую приносит им пользу.

![05](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/05.jpg)
На этом графике, который был взят мной [здесь](https://peter-chang.medium.com/ci-cd-continuous-integration-tools-delivery-react-web-travis-github-example-tutorial-javascript-vue-db8afe9f9a81), показан базовый рабочий процесс разработки Monero. Влияние работы MJ по компиляции и непрерывной интеграции очевидно при каждом проведении тестов.

**Могут ли действующие разработчики Monero оптимизировать процесс компиляции?**

Как разъяснил мне ситуацию MJ, над проектом Monero работал ряд узкоспециализированных разработчиков, многие из которых являются экспертами в определённых областях, таких как криптография, распределённые вычисления и так далее. Тем не менее оптимизация времени компиляции может просто отсутствовать в списке интересующих их вопросов. Он сталкивался с этой проблемой в случае и с другими проектами C++, над которыми работал в прошлом, а не только с Monero.

## _Повышение скорости компиляции_

Первым вкладом MJ в проект стала интеграция кэша компиляторов [Ccache](https://ccache.dev/). Это позволило ускорить компиляцию за счёт кэширования предшествующих компиляций с последующим обнаружением случаев проведения повторной компиляции и использованием её кэшированного двоичного файла вместо проведения новой компиляции с нуля.

Это сократило время непрерывной компиляции Travis примерно с 22 до 2 минут для каждой сборки ([источник](https://github.com/monero-project/monero/pull/6452#issuecomment-615024910)).

![06](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/06.jpg)
Здесь показано упомянутое выше повышение скорости за счёт использования Ccache.

Затем он продолжил работу над дальнейшей оптимизацией непрерывной интеграции, и вот два примера:
- сокращение времени выполнения ubuntu-test с 2 часов до 1 часа 25 минут (Pull [#7489](https://github.com/monero-project/monero/pull/7489));
- уменьшение размера кэшей, сохраняемых на GitHub, позволившее сократить частоту, с которой они вычищаются, а затем снова создаются с нуля (Pull [#7780](https://github.com/monero-project/monero/pull/7780)).

Прочие примеры работ, которыми поделился MJ:
- исправление проблемы, связанной с отказом сборки для Mac OSX с M1 CPU (Pull [#7435](https://github.com/monero-project/monero/pull/7435));
- помощь в переносе Monero на Rpi4, 64 бит (Pull [#7953](https://github.com/monero-project/monero/pull/7953));
- решение проблемы с UI для дистрибутивов  Mint и Void Linux: MJ не занимался непосредственно её устранением, но помог OP организовать мысли, провёл тестирование и описал, как можно воспроизвести проблему (Pull [#7862](https://github.com/monero-project/monero/issues/7862));
- решение проблемы со сборкой, о которой сообщил пользователь, пожелавший остаться анонимным (Pull [#7902](https://github.com/monero-project/monero/pull/7902));
- исправление проблемы с EasyLogging++, которая вызывала отказ приложения (Pull [#7828](https://github.com/monero-project/monero/pull/7828));
- также решение вопроса с EasyLogging++: добавление тестов Utest к предыдущему исправлению, внесённому Moo (Pull [#7771](https://github.com/monero-project/monero/pull/7771)).

## _Другие интересующие MJ области_

Надеюсь, вышеизложенное составило у вас представление о том, над чем в основном работал MJ-XMR. Ниже описаны ещё несколько интересующих его областей.

### _Анализ кода_

Всякий раз, когда подаётся пул-реквест, код проверяется сторонними людьми, и это позволяет убедиться в том, что он работает, как задумано, и ничего не нарушает в процессе выполнения. Как вы понимаете, далеко не все горят желанием анализировать чужой код. Но помощь, связанная с анализом кода, действительно способствует развитию проекта. В настоящее время очередью включения PR на GitHub управляет [selsta](https://github.com/selsta), и для selsta требуется дополнительная помощь с анализом кода, чтобы PR включались быстрее.

Конечно, MJ всё ещё новичок в проекте, поэтому без достаточно глубоких знаний кодовой базы он пока не может помочь с более сложными изменениями.

![07](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/07.png)
Пример утверждения пул-реквеста mj-xmr и ndorf после проведённого анализа ([ссылка](https://github.com/monero-project/monero/pull/8023))

### _Поддержка новых разработчиков_

MJ помогает новым разработчикам освоиться в проекте. Он занимается этим, общаясь с ними лично, один на один...

Например, под его недавним запросом о финансировании в CCS было приятно увидеть [комментарий JBerman](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/266#note_11779): «Также очень признателен @mj за его глубокое знание C++».

Он также помогает им путём улучшения документации, например:
- документации по эффективной компиляции, отладке и тестированию (Pull [#7666](https://github.com/monero-project/monero/pull/7666));
- документации по воспроизводимым сборкам (Gitian) (Pull [#7658](https://github.com/monero-project/monero/pull/7658/commits/834e23bfcf8eaabc0e41a7b51a9c35c8c08f11f0)).

### _Идеи на будущее_

MJ поделился, что на самом деле у него есть планы по целому ряду дальнейших оптимизаций, которые он хотел бы внести в проект, и среди которых:

- **Рефакторинг wallet2**

[wallet2.cpp](https://github.com/monero-project/monero/blob/master/src/wallet/wallet2.cpp) — это большой файл, состоящий более чем из 14 000 строк и содержащий основные функции кошелька. Он используется, например, в CLI и RPC, которые заключают его функции в оболочку (подробнее [читайте здесь](https://monero.stackexchange.com/questions/11415/what-is-the-difference-between-simplewallet-wallet-and-wallet2)).

![08](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/08.jpg)

В настоящее время в тестах MJ (см. [здесь](http://cryptog.hopto.org/monero/health/data/eec3a6014/eec3a6014-mem-usage-prod.txt)) файл wallet2.cpp является наиболее ресурсоёмким с точки зрения использования RAM при компиляции.

![09](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/09.jpg)

Это настоящая проблема для машин с небольшим объёмом оперативной памяти. Например, плата RPi4 с 4 ядрами и 4 Гб RAM может использовать только 1 ядро, чтобы избежать сбоев или интенсивной подкачки, которая может привести к повреждению её SD-карты.

Приведённый выше отчёт по RAM — это лишь один из отчётов, которые MJ регулярно генерирует после каждого ряда включений в кодовую базу Monero. Все они публикуются здесь: http://cryptog.hopto.org/monero/health/. Наличие всех прошлых отчётов облегчает отслеживание степени использования RAM или скорости компиляции с течением времени.

MJ хотел бы произвести рефакторинг кода wallet2.cpp и разбить его на файлы меньшего размера, сохраняя при этом существующие функциональные возможности без ущерба для чего-либо другого.

Это будет иметь два положительных последствия:
1. Уменьшится объём оперативной памяти, используемой машинами при компиляции проекта.
2. Файлы меньшего размера станут более доступными с точки зрения разработки. Особенно для начинающих разработчиков.

На данный момент он говорит, что такие неинвазивные, но решающие проблему изменения пока ещё не приняты (Pull [#7679](https://github.com/monero-project/monero/pull/7679)).

- **Добавление опережающих описаний в файлы заголовков**

![10](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/10.jpg)

Это поможет разрушить «каскадные зависимости», в результате чего мы получим:
1. Сокращение времени компиляций.
2. Меньшее количество перекомпиляций.

MJ предложил реализовать это в PR, однако в результате реально небольшие изменения были внесены примерно в 60 файлов (что достаточно много с точки зрения анализа), и PR принят не был. Тем не менее возможность реализовать это улучшение пока сохраняется.

- **Добавление модульных тестов для Mac и Windows в рабочий процесс GitHub Actions**

![11](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/11.jpg)

В настоящее время всякий раз, когда пул-реквест добавляется в ветку (главную или какую-то другую), выполняется рабочий процесс GitHub, реализующий все этапы компиляции, необходимые для двоичных файлов Linux, Mac и Windows. Это гарантирует, что вносимые изменения не нарушат процесс сборки. Кроме того, существует ряд тестов (на уровне ядра и модулей) для проверки отсутствия нарушений некоторых важных функций, однако они выполняются только в сборке Linux.

Обоснованием для выполнения тестов только в сборке Linux служит экономия времени и ресурсов сервера. При этом считается, что, поскольку код написан стандартным способом и может быть портирован, он будет вести себя одинаково на всех операционных системах. К сожалению, это не всегда так. В настоящее время команда ведущих разработчиков надеется на пользователей, отправляющих отчёты о возникающих проблемах и ошибках, а не на возможность их потенциального обнаружения до того, как они будут выявлены в MacOS и Windows.

В настоящее время выполнение модульных тестов занимает около 10 минут (см. скриншот ниже). Если бы были добавлены модульные тесты для MacOS и Windows, они бы выполнялись параллельно, поэтому время тестирования едва ли увеличилось бы, но потребовалось бы немного больше ресурсов.

![12](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/12.jpg)

## _Планы MJ-XMR по будущей работе_

В дальнейшем MJ продолжит свою текущую работу, но будет заниматься ей в меньшей степени, поскольку собирается активно работать над крупным проектом под названием OSPEAD:

### _Симулятор статистического анализа для OSPEAD_

Недавно новый контрибьютор сообщества Monero, Rucknium, выдвинул идею улучшения алгоритма выбора ложных выходов, используемого при создании кольцевых подписей.

Сегодня подписи Monero содержат кольцо, в которое входят 11 выходов, 10 из которых являются ложными и «случайным образом» выбираются из числа прошлых выходов, имеющихся в блокчейне. Rucknium напомнил сообществу (многие из участников которого уже были в курсе), что данный алгоритм выбора ложных выходов имеет статистическую уязвимость и нуждается в улучшении.

В настоящее время компания, занимающаяся анализом блокчейнов на основе повторяющихся шаблонов в данных, может попытаться и обоснованно предположить, какие из выходов в подписи являются ложными, а какие — реальными выходами. Конечно, этого нельзя знать наверняка.

И это представляет собой проблему, для решения которой требуется привлечение статистика, по сути, отсутствовавшего в проекте со времен изначального исследования, проведённого [Мёзером и др. (2018)](https://doi.org/10.1515/popets-2018-0025), и поэтому просто великолепно, что сейчас данный вопрос привлёк к себе некоторое внимание.

![13](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/12.jpg)

В рамках этого проекта Rucknium собрал «команду» разработчиков, которые должны помочь ему решить проблему. Среди них JBerman, UKoeHB и mj-xmr.

Роль MJ будет заключаться в предоставлении программного обеспечения и поддержке приложения, которое позволит Rucknium осуществлять моделирование с использованием новых алгоритмов и выявлять наличие слабых мест.

Это должно помочь избежать «сверхподгонки», когда алгоритм хорошо адаптирован для выборочного набора данных, но плохо работает в условиях реального мира.

Пожалуй, в данном случае было бы естественным задать вопрос: а как бы Rucknium выполнял свою часть работы без инструмента, разработанного mj-xmr? И этот вопрос поднимался на недавней встрече участников Исследовательской лаборатории Monero ([ссылка на журнал встречи](https://libera.monerologs.net/monero-research-lab/20211110)):

![14](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/13.jpg)

Что интересно, это говорит о том, что отчасти ценность такой реализации проекта будет заключаться в способности сотрудничать и в наличии второй пары глаз при рассмотрении проблемы. Я не знаю наверняка, но анализ данных с помощью временных рядов, по-видимому, является той нишевой областью, с которой далеко не каждый разработчик Monero сможет помочь Rucknium.

Другие преимущества сотрудничества включают в себя:
- сосредоточенность на скорости моделирования, снижающая риск возникновения компромиссов между пригодностью модели и временем, затрачиваемым на её обучение;
- быстрый обмен информацией и скорость обратной связи между исполнителем (MJ) и заказчиком (Rucknium). То, чего может быть трудно достичь в случае с другим программным обеспечением.

OSPEAD представляется очень важным проектом для Monero, поскольку он направлен на улучшение самой слабой части механизма обеспечения приватности Monero, и мне радостно наблюдать, как он развивается.

## _Краткое резюме MJ_

### _Предыдущий опыт разработки_

Несмотря на то, что MJ предпочитает отделять свою личность в «реальной жизни» от своей цифровой личности в проекте Monero, он поделился некоторой информацией о своем опыте работы в качестве технического специалиста:
- MJ работал в качестве разработчика в течение последних 13 лет;
- MJ имеет магистерскую степень в области вычислительной техники и специализируется на написании кода на объектно-ориентированных языках (в основном C++, который является языком, используемым в рамках проекта Monero);
- чтобы оплатить аренду жилья, MJ работал в различных областях, начиная с автоматизации процессов, картографических приложений для геоинформационных систем (GIS), использующих компьютерное зрение для навигации, и заканчивая многими другими видами проектов, связанными с математикой, проектированием или управлением вычислительными ресурсами;
- в качестве побочного проекта MJ разработал пару космических навигационных инструментов для реалистичного бесплатного симулятора космического полета, и инструменты были написаны на C++. Его текущий побочный проект представляет собой автоматизированную торговую и бэктестинговую платформу и также написан на C++.

### _Как он заинтересовался Monero_

Сначала MJ интересовало криптовалютное пространство в более широком понимании, и он просто занимался майнингом Bitcoin у себя дома.

Однако вскоре ему стало очевидно, что майнинг посредством ASIC довольно расточителен с точки зрения аппаратного обеспечения. С появлением каждого нового поколения майнеров Bitcoin (ASIC) образуется совсем небольшое временное окно, в рамках которого можно было бы окупить свои инвестиции и извлечь прибыль, после чего ваши ASIC неизбежно будут вытеснены более быстрым оборудованием. В результате ваши ASIC становятся простым мусором, а если вы покупаете ему на замену новые ASIC, прибыль заметно снижается.

![15](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/14.jpg)

С другой стороны, алгоритм RandomX позволяет пользователям заниматься майнингом Monero с помощью обычного CPU. Это оборудование, которое не устаревает полностью с появлением следующего поколения процессоров. Если вы прекращаете использовать процессор для майнинга, он по-прежнему может пригодиться для решения целого ряда других задач.

Интересно, как разные люди находят свой путь к Monero, так как изначально происходит это по самым разным причинам. Я полагаю, что Сергей Черных ([sech1](https://github.com/schernykh/)), создатель P2Pool, пула для децентрализованного майнинга, в своем [интервью MoneroTalk](https://www.youtube.com/watch?v=YjyPdyyidXE) упомянул, что он также попал в Monero из-за RandomX.

![16](/img/copyright/articles/2021-11-17-interview-with-mj-xmr/13.jpg)
Сергей Черных во время интервью MoneroTalk

## _Заключение_

Надеемся, что вышеизложенное поможет вам составить представление о том, над чем трудится один из новых разработчиков проекта Monero.

Без сомнения, по мере того как MJ продолжит свою работу над проектом и в ещё большей степени погрузится в него, он расширит свои таланты, и та польза, которую он сможет принести, только возрастёт.

Если у вас есть какие-либо вопросы, пожалуйста, задавайте их ниже в комментариях.

---

_Источник: ["Nightmare" - A Monero Fiction Short Story](https://rbrunner7.github.io/nightmare.html)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
