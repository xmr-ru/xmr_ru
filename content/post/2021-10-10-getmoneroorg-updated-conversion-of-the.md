---
title: "Обновление Getmonero.org: работа над преобразованием Moneropedia, новые посты в блогах, обновление FAQ, исправления и многое другое"
date: "2021-10-10"
categories:
  - "Новости"
tags:
  - "CCS"
lead: "Ежемесячный отчёт ErCiccione в ключе работы над его CCS предложением."
pager: true
toc: false
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

Привет всем! Много чего произошло на сайте в этом месяце. Работа над тем, чтобы Moneropedia стала переводимой (и масштабируемой), продолжается, но значительная её часть уже завершена. Мы также изменили страницу «Предприниматели» (Merchants), как и было обещано в последнем выпуске новостей. Теперь мы уделяем больше внимания P2P биржам, а предпринимателям отводится сторонняя директория, которую мы не будем сопровождать. Этот выпуск новостей закрывает мою [заявку в CCS](https://repo.getmonero.org/monero-project/ccs-proposals/-/merge_requests/241). Я собираюсь подать другую, но уже более гибкую. Заявка будет на три месяца, но работа будет распределяться в зависимости от моей занятости. Сейчас я нахожусь в процессе передачи некоторых моих обязанностей, связанных с проектом Monero и требующих значительных временных затрат. В результате я смогу уделять больше времени Haveno и прочим делам вне сети.

### _Обновление Getmonero_

После моего [последнего выпуска новостей](https://www.reddit.com/r/Monero/comments/p5caji/getmoneroorg_updated_big_changes_in_progress/) на [Getmonero.org](https://www.getmonero.org/) произошли следующие изменения:
- блог: добавлен пост, посвящённый свопам BTC → XMR ([#1789](https://github.com/monero-project/monero-site/pull/1789));
- добавлен пост, посвящённый реализации p2pool ([#1835](https://github.com/monero-project/monero-site/pull/1835));
- в целях согласованности изменены некоторые заголовки в руководстве пользователя ([#1769](https://github.com/monero-project/monero-site/pull/1769));
- блог: добавлены два поста, посвящённые версии v0.17.2.3 GUI и CLI ([#1801](https://github.com/monero-project/monero-site/pull/1801));
- инструменты: добавлена ссылка на MoneroLogs ([#1733](https://github.com/monero-project/monero-site/pull/1733));
- домашняя страница: под вводным видео добавлена ссылка на раздел FAQ «Существуют ли видео, которые помогут узнать больше о Monero?» ([#1795](https://github.com/monero-project/monero-site/pull/1795));
- добавлено руководство пользователя «Как произвести платёж» ([#1733](https://github.com/monero-project/monero-site/pull/1773));
- добавлен новый раздел FAQ «Что такое устойчивость к ASIC-майнингу? Почему она важна?» ([#1772](https://github.com/monero-project/monero-site/pull/1772));
- добавлена новая последовательность редакции и объединения пул-реквестов (связанных с проектами на GitHub) ([#1784](https://github.com/monero-project/monero-site/pull/1784));
- дорожная карта: статус «атомных свопов» изменён на завершённый ([#1793](https://github.com/monero-project/monero-site/pull/1793));
- ресурсы: обновлено руководство пользователя «Как восстановить кошелёк на основе мнемонической фразы» ([#1781](https://github.com/monero-project/monero-site/pull/1781));
- решены проблемы с высотой строки, из-за которых руководства разработчиков в некоторых случаях отображались неправильно ([#1808](https://github.com/monero-project/monero-site/pull/1808));
- руководства разработчиков: wallet-rpc — исправлен пример validate_address ([#1848](https://github.com/monero-project/monero-site/pull/1848));
- раздел FAQ: добавлена статья «Что такое максимальная денежная масса Monero?» ([#1818](https://github.com/monero-project/monero-site/pull/1818));
- руководства пользователей: после обновления restore_account.md обновлены все языковые файлы ([#1823](https://github.com/monero-project/monero-site/pull/1823));
- инструменты: добавлен раздел «Платёжные шлюзы» ([#1748](https://github.com/monero-project/monero-site/pull/1748));
- Moneropedia: удалена статья «Шифрование» ([#1837](https://github.com/monero-project/monero-site/pull/1837));
- раздел README: исправлен текст введения ([#1810](https://github.com/monero-project/monero-site/pull/1810));
- удалены файлы node., которые были сгенерированы по ошибке ([#1859](https://github.com/monero-project/monero-site/pull/1859)).

### _Реализация системы i18n для Moneropedia_

В прошедшем месяце большая часть моей деятельности была связана с рефакторингом Moneropedia с целью обеспечения возможности её перевода посредством Weblate (#1780). Это последняя составляющая, которая сделает сайт масштабируемым. Каждое из перечисленных PR преобразований является статьёй Moneropedia.
- https://github.com/monero-project/monero-site/pull/1796
- https://github.com/monero-project/monero-site/pull/1797
- https://github.com/monero-project/monero-site/pull/1799
- https://github.com/monero-project/monero-site/pull/1812
- https://github.com/monero-project/monero-site/pull/1809
- https://github.com/monero-project/monero-site/pull/1804
- https://github.com/monero-project/monero-site/pull/1800
- https://github.com/monero-project/monero-site/pull/1816
- https://github.com/monero-project/monero-site/pull/1821
- https://github.com/monero-project/monero-site/pull/1841
- https://github.com/monero-project/monero-site/pull/1843
- https://github.com/monero-project/monero-site/pull/1844
- https://github.com/monero-project/monero-site/pull/1847
- https://github.com/monero-project/monero-site/pull/1850
- https://github.com/monero-project/monero-site/pull/1814
- https://github.com/monero-project/monero-site/pull/1825
- https://github.com/monero-project/monero-site/pull/1826
- https://github.com/monero-project/monero-site/pull/1827
- https://github.com/monero-project/monero-site/pull/1830
- https://github.com/monero-project/monero-site/pull/1833
- https://github.com/monero-project/monero-site/pull/1834
- https://github.com/monero-project/monero-site/pull/1836
- https://github.com/monero-project/monero-site/pull/1839
- https://github.com/monero-project/monero-site/pull/1840

Данный список не содержит всех изменений, сделанных на веб-сайте или в репозитории. Более подробную информацию можно найти в [списки всех коммитов](https://github.com/monero-project/monero-site/commits/master) или [обзор активности на GitHub за последний месяц](https://github.com/monero-project/monero-site/pulse/monthly).

---

_Источник: [Getmonero.org updated: Conversion of the Moneropedia in progress, new blog posts, new FAQs, fixes and much more](https://www.reddit.com/r/Monero/comments/q53s1l/getmoneroorg_updated_conversion_of_the/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
