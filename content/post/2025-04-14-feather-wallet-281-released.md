---
title: "Релиз Feather Wallet 2.8.1"
date: "2025-04-14"
categories:
  - "Новости"
tags:
  - "Feather Wallet"
thumbnail: ""  
lead: "Состоялось обновление минималистичного некастодиального кошелька по типу Electrum, Feather Wallet, до версии 2.8.1"
pager: true
toc: true
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

## _Исправления и улучшения_

- Windows: исправлен сбой при запуске приложения кошелька, если путь к исполняемому файлу содержит Unicode символы.
- macOS: теперь, минимальная требуемая версия macOS 12.
  - В Qt v6.8.0 была прекращена поддержку macOS 11, что привело к ошибкам в Feather 2.8.0 при запуске приложения на macOS 11.
  - macOS 11 не поддерживается Apple уже более 18 месяцев. Всем пользователям настоятельно рекомендуется обновить свою операционную систему.
- Flatpak: теперь обрабатывает и использует тему курсора хоста.
  - Если после данного релиза у вас все еще возникают проблемы с курсором, убедитесь, что `/usr/share/icons/default/index.theme` не является символической ссылкой.

- Настройки: при попытке восстановить кошелёк из мнемонической фразы из 25 слов, Feather больше не должен ошибочно сообщать, что слово контрольной суммы недействительно.
- Сведения о компонентах: добавлена ​​вкладка, на которой отображаются номера версий некоторых компонентов кошелька.
- Revuo: добавлен разделитель между разделами "Последние новости" и "Предстоящие события".

- Qt обновлен до версии v6.9.0
- Tor обновлен до версии v0.4.8.16
- OpenSSL обновлен до версии v3.5.0

---

_Источник: [Feather Wallet 2.8.1 released](https://featherwallet.org/changelog/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
