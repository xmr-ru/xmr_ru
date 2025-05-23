---
title: "Релиз Feather Wallet 2.7.0"
date: "2024-10-08"
categories:
  - "Новости"
tags:
  - "Feather Wallet"
thumbnail: ""  
lead: "Состоялось обновление минималистичного некастодиального кошелька по типу Electrum, Feather Wallet, до версии 2.7.0"
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

## _Исправления и улучшения_

- история: всегда отображается интегрированный адрес в истории транзакций, если исходящая транзакция имеет идентификатор платежа
  - в некоторых случаях отображался некорректный адрес, когда платеж был совершен на интегрированный адрес
  - данная проблема могла привести к возможной потере средств, если был совершен повторный платеж в адрес какого-либо сервиса, а адрес был скопирован из диалога истории без проверки
  - **за сообщение об этой проблеме было [назначено вознаграждение](https://github.com/feather-wallet/feather/blob/master/SECURITY.md#bug-bounty-program) в размере 2.5 XMR**
  - на кошельках, поддерживающих аппаратные устройства Trezor, вместо этого отображается предупреждение, поскольку идентификатор платежа хранится на устройстве некорректно
- история: теперь вы можете импортировать описание транзакций из CSV-файла
- отправка: улучшено сообщение об ошибке, которое показывается, когда транзакция пытается потратить слишком много входов
- контакты: перевод контакту из адресной книги теперь автоматически заполняет имя контакта в описании транзакции
- монеты: «отправить себе» теперь отправляет средства на адрес текущего счета, а не на основной счет
- настройки: добавлена опция отображения фиатного баланса в статусбаре кошелька
- узлы: узлы, заканчивающиеся на '.local', теперь считаются локальными узлами
- узлы: добавлены узлы от участников сообщества - plowsof и ofrnxmr в список по умолчанию, удален hashvault
- мастер настройки: улучшено сообщение об ошибке, которое показывается, когда файл кэша не может быть прочитан
- мастер настройки: исправлена проблема с проверкой ввода на странице `set lookahead`, которая могла привести к сбою в работе приложения
- revuo: добавлены предстоящие события из календаря
- macos: исправлена проблема, из-за которой приложение не запускалось
- flatpak: даты, отображаемые в приложении, теперь должны отражать системное время
- добавление уведомлений о получении входящих транзакций за майнинг
- исправлена проблема, из-за которой приложение могло не закрываться
- исправлено несколько проблем с утечкой памяти
- Qt обновлен до версии 6.7.3
- OpenSSL обновлен до версии 3.3.2

---

_Источник: [Feather Wallet 2.7.0 released](https://featherwallet.org/changelog/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
