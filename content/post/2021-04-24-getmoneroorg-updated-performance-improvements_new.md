---
title: "Обновление Getmonero.org: повышение производительности, новые посты и раздел со «Списком мошенников»"
date: "2021-04-24"
categories:
  - "Новости"
tags:
  - "CCS"
lead: "Ежемесячный отчёт ErCiccione в ключе работы над его CCS предложением."
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

## _Обновления Getmonero_

Это основные изменения, внесённые в Getmonero.org с момента [последнего обновления](https://www.reddit.com/r/Monero/comments/m48tsw/getmoneroorg_updated_onion_address_one_new_faq/):
- После получения жалоб на появление мошеннических бирж, пытающихся использовать страницу «Предприниматели» для привлечения пользователей к их сервису, мы решили включать в свои списки меньше бирж и проводить более глубокую проверку. Следует отметить, что мы до сих пор не проводим какой-либо глубокой проверки, мы просто увеличили список критериев для включения в списки getmonero - [#1526](https://github.com/monero-project/monero-site/pull/1526), [#1518](https://github.com/monero-project/monero-site/pull/1518)
- За счёт добавления изображений с отложенной загрузкой была значительно улучшена работа некоторых страниц (экономия места составила до 54%. Подробности можно найти в PR) - [#1508](https://github.com/monero-project/monero-site/pull/1508)
- Был добавлен пост с объявлением о выходе версии v0.17.2.0 - [#1564](https://github.com/monero-project/monero-site/pull/1564)
- Был добавлен пост с объявлением о выходе версии v0.17.2.1 - [#1574](https://github.com/monero-project/monero-site/pull/1574)
- В библиотеку был добавлен раздел со списком мошенников - [#1522](https://github.com/monero-project/monero-site/pull/1522)
- Также в библиотеку добавлен список мошеннических колец - [#1496](https://github.com/monero-project/monero-site/pull/1496)
- Руководства пользователя были полностью переведены на норвежский язык - [#1492](https://github.com/monero-project/monero-site/pull/1492), [#1493](https://github.com/monero-project/monero-site/pull/1493)
- Были добавлены переводы из Weblate - [#1466](https://github.com/monero-project/monero-site/pull/1466)
- Была обновлена страница Что такое Monero. Также были добавлены командные кнопки - [#1481](https://github.com/monero-project/monero-site/pull/1481), [#1506](https://github.com/monero-project/monero-site/pull/1506)
- Был активирован новый норвежский язык - [#1511](https://github.com/monero-project/monero-site/pull/1506)
- Был добавлен пост с объявлением о новом доступном языке (норвежском) - [#1541](https://github.com/monero-project/monero-site/pull/1541)
- Почти все руководства пользователя были преобразованы, чтобы их можно было переводить на Weblate. Все наши действия можно отследить на [#1270](https://github.com/monero-project/monero-site/pull/1270) - [#1530](https://github.com/monero-project/monero-site/pull/1530), [#1531](https://github.com/monero-project/monero-site/pull/1531), [#1538](https://github.com/monero-project/monero-site/pull/1538), [#1539](https://github.com/monero-project/monero-site/pull/1539), [#1540](https://github.com/monero-project/monero-site/pull/1540)
- К промовидео на главной странице были добавлены итальянские субтитры - [#1450](https://github.com/monero-project/monero-site/pull/1450)
- Был исправлен механизм переключения языка на английский при выборе категории - [#1527](https://github.com/monero-project/monero-site/pull/1527)
- На страницу загрузок был добавлен раздел «Антивирус» - [#1500](https://github.com/monero-project/monero-site/pull/1500)
- Были задокументированы все параметры для rpc вызовов export_outputs и export_key_images - [#1505](https://github.com/monero-project/monero-site/pull/1505)
- Исправлена ошибка, из-за которой панель навигации не отображалась на определённых дисплеях - [#1504](https://github.com/monero-project/monero-site/pull/1504)
- Была добавлена стрелка/кнопка прокрутки вверх, а также раскрывающееся меню страницы «Предприниматели» - [#1502](https://github.com/monero-project/monero-site/pull/1502)
- Были изменены некоторые формулировки на странице «О нас» - [#1501](https://github.com/monero-project/monero-site/pull/1501)
- В руководстве разработчика wallet-rpc были удалены несуществующие параметры - [#1499](https://github.com/monero-project/monero-site/pull/1499)
- Пункт «луковые адреса» в дорожной карте был отмечен как «завершённый» - [#1491](https://github.com/monero-project/monero-site/pull/1491)
- Были стандартизированы гиперссылки на видео в разделе FAQ - [#1476](https://github.com/monero-project/monero-site/pull/1476)
- Были внесены минимальные исправления в руководство пользователя daemon-rpc - [#1425](https://github.com/monero-project/monero-site/pull/1425)
- Домен комнат Matrix на странице «Общение» был изменён на monero.social - [#1479](https://github.com/monero-project/monero-site/pull/1479)
- Пункт, касающийся аппаратного кошелька Kastelo, был удалён из дорожной карты - [#1542](https://github.com/monero-project/monero-site/pull/1542)
- На странице «Пресс-кит» была удалена лишняя ссылка на monerooutreach.org - [#1507](https://github.com/monero-project/monero-site/pull/1507)
- Новые контрибьюторы помогли исправить некоторые незначительные проблемы, в том числе опечатки в разделах CCS. Большое им за это спасибо :) - [#1546](https://github.com/monero-project/monero-site/pull/1546), [#1557](https://github.com/monero-project/monero-site/pull/1557), [#1556](https://github.com/monero-project/monero-site/pull/1556), [#1554](https://github.com/monero-project/monero-site/pull/1554), [#1551](https://github.com/monero-project/monero-site/pull/1551), [#1548](https://github.com/monero-project/monero-site/pull/1548), [#1547](https://github.com/monero-project/monero-site/pull/1547), [#1572](https://github.com/monero-project/monero-site/pull/1572), [#1534](https://github.com/monero-project/monero-site/pull/1534), [#1513](https://github.com/monero-project/monero-site/pull/1513)

Данный список не включает в себя всех изменений, внесённых в разделы веб-сайта или в репозиторий. Чтобы получить более подробную информацию, ознакомьтесь со [списком всех коммитов](https://github.com/monero-project/monero-site/commits/master) или [историей случившегося на Github в течение последнего месяца](https://github.com/monero-project/monero-site/pulse/monthly).

## _Новые предприниматели_

Это список компаний, которые принимают Monero и были недавно добавлены на страницу «Предприниматели». Полный список можно найти по этой ссылке: https://www.getmonero.org/community/merchants/.

Примечание: мы даём ссылки этих предпринимателей исключительно для удобства, но не проводим никакой проверки. Единственное, что мы проверяем, действительно ли эти веб-сайты принимают Monero и не являются ли они мошенническими. Не пользуйтесь данными сервисами, предварительно не проверив их самостоятельно.

**digitalgoods от ProxyStore** [#1536](https://github.com/monero-project/monero-site/pull/1536)

Цифровые товары, такие как коды Mullvad VPN

https://digitalgoods.proxysto.re/

---

**TrilightZone** [#1520](https://github.com/monero-project/monero-site/pull/1520)

Предоставление анонимных офшорных услуг с 2005 года

https://trilightzone.org/

---

**CoinCat** [#1516](https://github.com/monero-project/monero-site/pull/1516)

Покупка и продажа криптовалют за считанные минуты

https://coincat.in/

---

**1984 Hosting Iceland** [#1512](https://github.com/monero-project/monero-site/pull/1512)

Хостинг для озабоченных проблемами конфиденциальности борцов за свободу

https://1984hosting.com

---

3 компании было удалено из списка: [#1515](https://github.com/monero-project/monero-site/pull/1515), [#1514](https://github.com/monero-project/monero-site/pull/1514), [#1580](https://github.com/monero-project/monero-site/pull/1580)

Если вы знаете компанию, которая принимает Monero, но не указана в списке, сообщите нам, и мы добавим её на страницу Предприниматели. Чтобы добавить компанию в список, создайте запрос в репозитории и заполните соответствующую форму.

---

_Источник: [Getmonero.org updated: Performance improvements, new blog posts, new 'Cheatsheets' section, a lot of improvements and fixes and much more](https://www.reddit.com/r/Monero/comments/mxko4r/getmoneroorg_updated_performance_improvements_new/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
