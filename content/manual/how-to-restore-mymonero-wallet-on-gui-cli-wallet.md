---
title: "Как восстановить аккаунт MyMonero в локальном кошельке CLI / GUI"
categories:
  - "Руководства"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

Веб-кошельки не являются безопасным местом для хранения ваших средств, и MyMonero.com не исключение. В этом мануале рассмотрим как восстановить аккаунт MyMonero.com в локальном кошельке.

MyMonero-кошельки используют другой тип мнемонической фразы - 13 слов (вместо 25-ти), которые не поддерживаются в Monero Core. Есть вариант с импортированием ключей в локальный кошелек.

Зайдя в свой MyMonero-аккаунт, в правом верхнем углу жмите на `Account → Account Details`.

![01](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/01.png)

Появится окно с ключами от вашего аккаунта:

![02](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/02.png)

## _CLI_

Для того чтобы начать процесс импорта ключей, достаточно запустить **monero-wallet-cli** с ключом `--generate-from keys` и дать имя новому файлу кошелька, пример:
```
./monero-wallet-cli --generate-from-keys MyMonero.XMR.RU
```

 _**Примечание**: Если вы используете удаленную ноду, тогда поле название кошелька вам нужно указать саму ноду, пример_:
```
./monero-wallet-cli --generate-from-keys MyMonero.XMR.RU --daemon-address node.moneroworld.com:18089
```


Кошелек попросит ввести по очереди **Standard address**;**Secret spend key**; **Secret view key**, а также создать пароль для кошелька.

`Restore from specific blockchain height (optional, default 0), or alternatively from specific date (YYYY-MM-DD)` - здесь можно указать высоту блокчейна (или дату), с которой начнется синхронизация кошелька. Если вы не знаете точной или приблизительной высоты блокчейна, когда вы получили средства, тогда просто нажмите клавишу Enter, кошелек начнет синхронизацию с первого блока.

В этом примере, я указал дату 10 сентября 2017 года. Кошелек показал мне высоту блокчейна 1394200 и попросил подтверждения.

![03](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/03.png)

На скриншоте трудно не заметить сообщение после команды seed:

**Error: wallet is non-deterministic and has no seed**

Вспомните начало данного мануала - Monero Core не поддерживает восстановление по мнемонической фразе из MyMonero.com. Поэтому рекомендуется создать новый кошелек, и переслать туда свои XMR. Тогда у вас будет мнемоническая фраза из 25 слов, которую проще и безопаснее хранить, чем три ключа с MyMonero.com


## _GUI_

С импортированием ключей в Monero Core GUI тоже не должно возникнуть проблем.

Открываете кошелек и выбираете язык:

![04](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/04.png)

Выбираете **Restore wallet from keys or mnemonic seed** (Восстановить кошелек с помощью ключей или мнемонической фразы):

![05](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/05.png)

В следующем окне нужно выбрать **Restore from keys** (Восстановить с помощью ключей) и собственно ввести ключи от MyMonero-аккаунта:

![06](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/06.png)

![07](/img/manuals/how-to-restore-mymonero-wallet-on-gui-cli-wallet/07.png)

Вот и все. Надеюсь что этот мануал будет кому то полезен.
