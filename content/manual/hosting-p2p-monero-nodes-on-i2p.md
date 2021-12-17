---
title: "Хостинг p2p узла Monero в I2P"
categories:
  - "Руководства"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

Настоящий документ является кратким руководством для тех операторов новых и/или существующих узлов Monero, которые хотят поддержать пользователей I2P, позволив их узлам передавать p2p данные через I2P.

После того как вы прочитаете этот документ, вы сможете создать I2P узел примерно за 20 минут.

## _Требования_
- система Linux, которая может быть защищена firewall (то есть домашняя сеть);
- последняя версия Monero (CLI), [ссылка](https://downloads.getmonero.org/cli/linux64);
- последняя версия I2P-Zero (на момент написания — v1.12), [ссылка](https://github.com/i2p-zero/i2p-zero/releases).

## _I2P-Zero_

I2P-Zero (также называется i2pz) — это небольшой футпринт I2P маршрутизатора. Эта программа сократилась до встраиваемой среды выполнения Java и не имеет зависимостей как таковых.

У неё есть контрольный порт 8051, который можно использовать для создания службы (служб) I2P. Это простой текстовый протокол. Для взаимодействия следует использовать tunnel-control.sh или, как вариант, просто использовать: netcat: echo -e "version" | nc 127.0.0.1 8051.

I2P-Zero имеет GUI, но не будет использовать его, так как, наиболее вероятно, вы будете устанавливать программу на сервер.

Если кратко, I2P-Zero позволяет:
- Разместить eepsite (веб-сайт I2P).
- Разместить любую службу в сети I2P (например, направить локальный DNS-сервер на 127.0.0.1:53, чтобы обеспечить к нему доступ по I2P).
- Создать локальный прокси-сервер SOCKS, который можно будет использовать для направления трафика в туннель.

Наша цель состоит в размещении полного рабочего узла через I2P, поэтому нам необходимо конфигурировать как входящий, так и исходящий I2P трафик:
- для размещения monerod через I2P нам понадобится воспользоваться опцией 2;
- для перенаправления трафика через I2P нам понадобится воспользоваться опцией 3.

## _Установка I2P-Zero_

- Распаковать и переместить в i2p-zero-linux.vX.XX/router/bin.
- Запустить процесс I2P-Zero: ./launch.sh.
- ???
- w00t!!

Убедиться в том, что программа использует netstat -tulpn | grep '8051' (мы производим обработку, используя grep, для контрольного порта).

### I2P-Zero systemd

Для /etc/systemd/system/i2pzero.service существует скрипт запуска systemd:
```
[Unit]
Description=i2pzero

[Service]
Type=simple
ExecStart=/bin/bash /home/i2pz/i2p-zero-linux.v1.10/router/bin/launch.sh
User=i2pz
Group=i2pz

[Install]
WantedBy=multi-user.target
```

Изменить пути по желанию, перезагрузить `systemd: systemctl daemon-reload`, после чего можно выполнить `service i2pzero start`.

Убедиться в том, что всё работает: `netstat -tulpn | grep '8051'`.

### _Конфигурирование I2P-Zero: создание сервера_

Сначала нам необходимо зарегистрировать I2P службу/сервер:
```
./tunnel-control.sh server.create 127.0.0.1 48083
```

на выходе вы получите I2P адрес b32, например:
```
suspiciouslyrandomandverylongstring.b32.i2p
```

Это будет адрес вашего I2P сервера/службы, который будет использоваться для входящих соединений.

### _Конфигурирование I2P-Zero: создание туннеля SOCKS_

Чтобы наш узел мог ретранслировать входящие транзакции по I2P, нам необходимо создать выходящие соединения по I2P. Чтобы направить трафик в I2P, нам понадобится создать туннель SOCKS. I2P-Zero позволяет сделать это.

Для создания туннеля SOCKS выполняется следующая команда:
```
./tunnel-control.sh socks.create 48085
```

I2P-Zero подтвердит создание этого туннеля простым OK.

Для мониторинга туннеля используется
```
./tunnel-control.sh all.list | python -m json.tool.
```

## _Запуск monerod_

Пришло время запустить monerod. Нам необходимо включить следующий флаг: `--anonymous-inbound` ([документация](https://github.com/monero-project/monero/blob/master/ANONYMITY_NETWORKS.md#inbound-connections)), чтобы monerod знал «публичный» адрес и порт нашего I2P сервера.

Формат будет следующим:
```
--anonymous-inbound <address>,127.0.0.1:<M>
```

где `M` будет свободным локальным портом, а адресом — ваш адрес _b32.i2p_.

Ранее нашему I2P серверу нами был назначен порт 48083. Наш флаг становится следующим:
```
--anonymous-inbound "suspiciouslyrandomandverylongstring.b32.i2p,127.0.0.1:48083"[HTML]
```

Другим флагом, который необходимо включить, будет --proxy (документация). Если не включить этот флаг, ваш узел не сможет ретранслировать транзакции в сеть I2P. Данный флаг должен включаться всегда.
```
--proxy i2p,127.0.0.1:48085
```

Последним необходимым флагом является `--add-peer`, который указывает на существующий сид-узел I2P (также называемый mipseed), к которому можно подсоединиться. Без этой команды вы не сможете ретранслировать транзакции, так как вы не будете подсоединены к какому-либо узлу.

```
--add-peer "dsc7fyzzultm7y6pmx2avu6tze3usc7d27nkbzs5qwuujplxcmzq.b32.i2p"
```

### _Monero Daemon systemd_

Для `/etc/systemd/system/monerod.service` существует скрипт запуска systemd:
```
[Unit]
Description=monerod
After=network.target

[Service]
Type=forking
PIDFile=/home/monero/monerod.pid
ExecStart=/home/monero/monero-x86_64-linux-gnu.0.14.1.0/monerod --anonymous-inbound "suspiciouslyrandomandverylongstring.b32.i2p,127.0.0.1:48083" --restricted-rpc --detach --pidfile /home/monero/monerod.pid
User=monero
Group=monero

[Install]
WantedBy=multi-user.target
```

Вы можете изменить его по собственному усмотрению.

## _Заключение_

Подытожим. Вышеуказанные 3 флага (`--anonymous-inbound`, `--proxy`, `--add-peer`) необходимы для того, чтобы программа I2P-Zero обеспечила возможность размещения узла Monero.

Для понимания я опубликую полную команду monerod, которую лично я использую со своим публичным узлом RPC Monero на сервере:
```
./monerod
 --max-concurrency 4 \
 --rpc-bind-ip YOUR.IP \
 --rpc-bind-port 18089 \
 --restricted-rpc \
 --public-node \
 --anonymous-inbound "suspiciouslyrandomandverylongstring.b32.i2p,127.0.0.1:48083" \
 --proxy i2p,127.0.0.1:48085 \
 --add-peer "dsc7fyzzultm7y6pmx2avu6tze3usc7d27nkbzs5qwuujplxcmzq.b32.i2p" \
 --confirm-external-bind
```

Что ещё можно прочитать по теме:
- [страница проекта I2P-Zero](https://github.com/i2p-zero/i2p-zero);
- [Трансляция транзакций через скрытую службу Tor, предложение в CCS](https://ccs.getmonero.org/proposals/vtnerd-tor-tx-broadcasting.html) (опубликовано vtnerd).
