---
title: "Коротко о мультиподписях Monero: как мгновенно создать MMS с нуля"
categories:
  - "Руководства"
thumbnail: "/img/manuals/monero-multisig-run-through-zero-to-mms-in-an-instant/01.png"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

Мультиподписи Monero только кажутся страшными. Чтобы показать, насколько быстро они создаются, я воспользуюсь отрывком из соответствующего руководства пользователя и на его основе создам собственное, пожалуй, самое краткое руководство по мультиподписям Monero.

## _Установка и конфигурирование PyBitmessage​_

Представим, что протокол _Bitmessage_ — это чат-рум, где ваши клиенты Monero собираются, чтобы обменяться информацией, необходимой для каждого последующего шага. Мы настраиваем её как демон, который сможет использовать monero-wallet-cli.
```
# Install required applications (example for Arch Linux)
sudo pacman -S python2 openssl git

# Download PyBitmessage
git clone https://github.com/Bitmessage/PyBitmessage.git
cd PyBitmessage

# Check if core dependencies are met.
# You may disregard any warnings about missing Qt.
python2 checkdeps.py

# Install PyBitmessage
python2 setup.py install --user

# Execute PyBitmessage once to generate config files
python2 ~/.local/bin/pybitmessage -h

# Enable daemon mode and disable Dandelion
[ -z $XDG_CONFIG_HOME ] && XDG_CONFIG_HOME="$HOME/.config"
echo 'daemon = true\n[network]\ndandelion = 0' >> ${XDG_CONFIG_HOME}/PyBitmessage/keys.dat

# Execute PyBitmessage
python2 ~/.local/bin/pybitmessage

# Generate your Bitmessage address
python_code='import xmlrpclib, json, time ;
api = xmlrpclib.ServerProxy("http://username:password@localhost:8442/") ;
print api.createRandomAddress("")'
transport_address=`echo ${python_code} | python2`
echo ${transport_address}
```

Придерживаясь вышеупомянутой аналогии с чат-румом, ваш транспортный адрес можно рассматривать в качестве псевдонима, которым вы пользуетесь в чате Bitmessage. Нашим следующим шагом является раскрытие этого псевдонима клиенту Monero.

## _Настройка multisig-кошелька (клиент Monero со стороны Элис)​_

В случае с monero-wallet-cli используются следующие команды.

### _Снижение уровня интерактивности monero-wallet-cli_

```
set ask-password 0
set inactivity-lock-timeout 0
```

### _Инициализация multisig Элис_

Укажите необходимый вам тип мультиподписи и назовите дополнительных подписантов.
```
mms init 2/2 alice PUT_ALICES_TRANSPORT_ADDRESS_HERE
mms set auto-send 1
mms signer 2 bob
mms start_auto_config
```

После ввода последней команды вы увидите токен в формате _mmsXXXXXXXX_. Необходимо передать этот токен Бобу. Он понадобится ему на следующем этапе.

## _Настройка multisig-кошелька (со стороны Боба)​_

Как и Элис, Бобу необходимо настроить PyBitmessage (см. выше), а затем создать Bitmessage адрес:
```
python_code='import xmlrpclib, json, time ;

api = xmlrpclib.ServerProxy("http://username:password@localhost:8442/") ;
print api.createRandomAddress("")'
echo ${python_code} | python2
```

### _Снижение уровня интерактивности клиента Monero со стороны Боба_

```
set ask-password 0
set inactivity-lock-timeout 0
```

### _Инициализация multisig со стороны Боба_

Необходимо использовать следующие команды, вставив правильный адрес Боба и заменив mmsXXXXXXXX на токен, полученный от Элис.
```
mms init 2/2 bob   PUT_BOBS_TRANSPORT_ADDRESS_HERE
mms set auto-send 1
mms auto_config mmsXXXXXXXX
```

## _Элис: отправка необходимых данных подписантам посредством Bitmessage​_

Как только MMS получит новое сообщение на клиент Monero Элис, следует дважды ввести команду mms next:
```
mms next
mms next
```

После первой команды будут отправлены данные конфигурации подписанта, а после второй — набор ключей.

## _Боб: отправка необходимых данных посредством Bitmessage​_

Как только MMS получит новое сообщение на клиент Monero Боба, следует трижды ввести команду mms next:
```
mms next
mms next
mms next
```

После первой команды будут обработаны данные конфигурации подписанта, после второй — отправлен набор ключей, а после третьей команды будет завершено создание multisig-адреса для Боба.

## _Элис: отправка необходимых данных подписантам посредством Bitmessage​_

Необходимо ещё раз ввести mms next:
```
mms next
```

Ввод этой команды завершит создание multisig-адреса для Элис.

## _Ваша первая multisig-транзакция​_

Теперь отображаемый адрес Monero должен поменяться на новый, который будет одинаковым для клиентов Боба и Элис.

**Как только на этот счёт поступят какие-либо средства (то есть как только вы положите на него сколько-нибудь XMR), вы сможете отправлять средства другим пользователям.**

Для запуска передачи следует использовать команду mms transfer RECIPIENT_ADDRESS AMOUNT. Затем с обеих сторон необходимо вводить команду mms next до тех пор, пока команда не обозначит, что уже больше ничего делать не требуется.

Следует отметить, что доставка сообщений Bitmessage обычно задерживается на несколько минут. Если произойдёт «затор», следует использовать команду mms list, которая покажет, должно ли на этом этапе прийти очередное сообщение.
