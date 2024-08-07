---
title: "TheCharlatan - Атомные свопы: настоящее и будущее протокола Farcaster"
date: "2022-06-18"
categories:
  - "Стенограмма"
tags:
  - "MoneroKon 2022"
lead: "Monero Konferenco 2022 #MoneroKon2022 Лиссабон - День 1 | 'Молниеносная' сессия 1"
pager: true
toc: false
sidebar: "right"
---

{{< youtube id="KbR77ffo-nQ" autoplay="false" >}}

---

Я  собираюсь рассказать о Farcaster, программном обеспечении для совершения свопов Bitcoin-Monero. Farcaster использует микросервисы, реализованные на языке Rust, а также криптографию. И я буду говорить о прошлом, настоящем и будущем этого программного обеспечения.

Если кратко, проект Farcaster финансируется через систему CCS. Цель состоит в реализации атомных свопов Bitcoin-Monero. Изначально над проектом работала швейцарская компания Crypt GmbH, на которую работаю я, и которая занимается разработкой и исследованиями в криптовалютной сфере. Это открытый проект с лицензией MIT. Мы изложили спецификации протокола и программного обеспечения в RFC из 9 частей.

Также кратко расскажу, что такое атомные свопы. При совершении обычного свопа, как правило, требуется привлечение третьей стороны, действующей в качестве арбитра и предотвращающей возможность обмана при совершении свопа. И в какой-то момент средства находятся на хранении у такого арбитра. Вместо арбитра атомные свопы используют криптографические механизмы, исключающие возможность мошенничества.

Финансирование Farcaster в CCS проходило с большим энтузиазмом. Первоначально ожидалось, что готовое программное обеспечение появится в 1-м и 2-м кварталах 2021 года, а бюджетом была предусмотрена работа пяти разработчиков. Однако на данный момент мы выполнили 10 или 16 этапов, так что реализация проекта запаздывает, и теперь он будет завершён в 2022 году. Над проектом также никогда не работало более 3 разработчиков одновременно. Кроме того, мы завершили реализацию представленных коммитами атомных свопов Bitcoin-Monero, хотя соответствующее программное обеспечение в настоящее время не поддерживается.

Помимо того, что на данный момент не поддерживаются коммиты, есть и другие веские причины, почему мы продолжаем продвигать этот проект. Во-первых, реализация свопов Farcaster симметрична, она позволяет как покупать, так и продавать XMR и BTC, то есть, работает в обе стороны. Также по завершении свопа можно перевести Monero на указанный адрес. Основная архитектура и основная библиотека Farcaster расширяемы, что позволяет добавлять и другие активы в будущем. Мы построили всё с помощью этой масштабируемой архитектуры микросервисов. Мы также поддерживаем сервер лёгкого кошелька Monero и разработали сайт forecaster.dev, который автоматически выводит имеющиеся предложения по совершению свопов.

В целом наша архитектура - это реализованные на Rust микросервисы, которые могут обмениваться друг с другом информацией, используя сообщения класса ZeroMQ. Эти сервисы изолированы функциями, поэтому у нас имеется отдельный сервис, отвечающий за машину состояния свопа, сервис для конкретной криптографической модели, базы данных и так далее. И всеми этими сервисами можно управлять с помощью одного приложения с поддержкой командной строки.

В настоящее время мы собираемся выйти в основную сеть. Скоро. А если серьёзно, это должно произойти в течение 1-2 месяцев. Так что следите за новостями, публикуемыми в субреддите Monero. Что мы действительно сделали на данный момент, мы обеспечили возможность восстановления средств пользователями при любых обстоятельствах. Это особенно важно, если учесть опыт наших конкурентов, у которых пользователи попадали в настоящие неприятности, когда дело доходило до восстановления средств, а также опыт ранней версии Lightning Network, тогда я и сам испытал некоторые сложности, так как мне пришлось восстанавливать средства из «мёртвого» канала. Работа над API почти завершена, и в ближайшее время мы приступим к разработке GUI.

В будущем мы собираемся решить проблему «свободной опции». Эта проблема возникает из-за того, что в рамках нашего протокола Bitcoin всегда блокируется первым, а это значит, что тот, кто хочет совершить своп, всегда первым блокирует Bitcoin и, следовательно, вынужден уплатить минимум одну комиссию за транзакцию, не зная, совершит ли своп другая сторона. Мы стремимся решить эту проблему, либо путём предварительной уплаты комиссии доверенным контрагентом, с помощью задержки и доказательства обладания средствами, либо за счёт реализации «репутационных сетей» поверх Farcaster. Я также занимался разработкой процесса построения цепочек транзакций Monero, и на конференции будет ещё одно выступление, в котором эта тема будет рассмотрена более подробно. И, очевидно, мы хотим в какой-то момент реализовать возможность совершения свопов не только с Bitcoin, но и другими активами. Спасибо.
