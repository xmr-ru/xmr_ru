---
title: "Релиз Feather Wallet 2.1.0"
date: "2022-08-12"
categories:
  - "Новости"
tags:
  - "Feather Wallet"
thumbnail: ""  
lead: "Состоялось обновление минималистичного некастодиального кошелька Feather Wallet до версии 2.1.0."
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

## _Примечания_

Пользователи Windows, установившие Feather Wallet с помощью программы установки, должны выполнить обновление вручную. Загрузите актуальный установщик 2.1.0 с [featherwallet.org/download](https://featherwallet.org/download/) и следуйте инструкциям установщика.

Сборки для macOS теперь кросс-компилируются и воспроизводятся автоматически. Работа по переносу системы сборки на Guix + `depends` была упразднена из-за постоянной ошибки с собственными нестатическими сборками. Это существенное изменение, которое может непреднамеренно вызвать проблемы с совместимостью в некоторых версиях macOS. Если вы ранее могли запускать Feather, но не можете запустить 2.1.0, пожалуйста, [сообщите нам об этом](https://docs.featherwallet.org/guides/report-an-issue).

Все двоичные файлы выпуска, кроме macOS, были созданы с использованием Docker. Мы будем постепенно отказываться от сборок Docker в пользу загрузочных сборок Guix в будущих выпусках (после проведения дополнительного тестирования).

Пожалуйста, обратите внимание, что все версии Feather 1.0.1 и ниже перестанут работать после планового хардфорка (13 августа). Обязательно обновите свой кошелек до версии 2.0.0 или более новой, прежде чем обращаться в службу поддержки.

## _Исправления_

- Отправка всего расходуемого остатка кошелька на интегрированный адрес больше не должна вызывать критическую ошибку в работе кошелька.
- Исправлена ошибка, из-за которой встроенное средство обновления не могло установить актуальную версию Feather Wallet (установщик Windows).
- Исправлена ошибка с зависанием при импорте транзакции в пользовательском интерфейсе кошелька.

## _Сопровождение_

- Обновление Monero до версии 0.18.1.0.

## _Известные проблемы_

- macOS: Сканер QR-кодов с веб-камеры не работает в этой версии кошелька.

---

_Источник: [Feather Wallet 2.1.0 released](https://www.reddit.com/r/FeatherWallet/comments/wmly8h/feather_wallet_210_released/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
