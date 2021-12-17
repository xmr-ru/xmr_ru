---
title: "Как запустить собственный удаленный узел Monero на VPS"
categories:
  - "Руководства"
comments: false
authorbox: false
pager: true
toc: false
mathjax: true
sidebar: "right"
---

## _Что такое monerod?_

`monerod` является демон-программой в составе Monero. Это консольная программа, используемая для управления блокчейном. Если кошелек Bitcoin позволяет управлять как кошельком, так и блокчейном, то в Monero эти функции разделены: `monerod` работает с блокчейном, а `monero-wallet-cli` управляет кошельком.

Настоящее руководство подразумевает, что у вас уже создан VPS сервер, и вы используете SSH для получения доступа к консоли данного сервера.

## _Linux, 64-bit (Ubuntu 16.04 LTS)_

#### - _Убедитесь в том, что порт 18080 открыт_

`monerod` использует порт 18080 для связи с другими узлами в сети Monero.

Пример использования `ufw`: `sudo ufw allow 18080`
Пример использования `iptables`: `sudo iptables -A INPUT -p tcp --dport 18080 -j ACCEPT`

#### - _Загрузить актуальные двоичные файлы Monero Core_

`wget https://downloads.getmonero.org/linux64`

#### - _Создать директорию и извлечь файлы_
```
mkdir monero
tar -xjvf linux64 -C monero
```
#### - _Запустить демон-программу_
```
cd monero
./monerod
```
#### - _Опции_:

Открыть список всех опций и настроек:

`./monerod --help`

Запустить демон-программу фоновым процессом:

`./monerod --detach`

Следить за результатом вывода `monerod` при запуске в качестве демон-программы:

`tail -f ~/.bitmonero/bitmonero.log`

Обезопасить VPS посредством автоматического обновления:

https://help.ubuntu.com/community/AutomaticSecurityUpdates
