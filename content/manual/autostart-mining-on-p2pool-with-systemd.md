---
title: "Как начать майнинг на пуле с помощью XMRig"
categories:
  - "Руководства"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

## _Введение​_

Мне доводилось сталкиваться с постами, посвящёнными перезапуску xmrig, автозапуску p2pool и многому другому. Но я никогда не читал поста, описывающего более или менее надёжные способы настройки всех этих функций, и поэтому я решил написать именно такой пост.

### _Требования_

- Наличие Linux с root-доступом (само собой разумеется).
- Наличие пакета systemd (используется многими дистрибутивами, так что есть высокая вероятность того, что у новичков он уже будет установлен).

### _Что будет установлено_

- Monerod, P2Pool, Xmrig - то есть всё, что нужно для майнинга в P2Pool.

### _Отказ от ответственности_

Я старался сделать это руководство настолько полным и качественным, насколько было возможно, но не исключено, что всё же я где-то напортачил.
Также следует быть осторожными при копировании команд из интернета.

## _Подготовка_

Из соображений безопасности было бы лучше, чтобы процессы p2pool и monerod запускались с отдельных, непривилегированных учётных записей. Xmrig является исключением, поскольку запускается с правами суперпользователя root, позволяющими производить некоторую оптимизацию, а, как известно, чем больше XMR будет нами получено, тем лучше.

Создание учётной записи является опцией - в этом нет никакой необходимости с точки зрения майнинга, но довольно предусмотрительно в плане безопасности.

Поэтому рекомендуется завести по отдельной учётной записи для каждого демона. Создать их можно следующим образом:
```
sudo useradd --user-group --home-dir=/opt/p2poold p2poold;
sudo useradd --user-group --home-dir=/opt/monerod monerod;
```

Опция `--home-dir` поможет в том случае, если вы не хотите, чтобы учётные записи ваших демонов имели домашнюю директорию в /home и засоряли её (но, опять же, это лишь опция). Я использовал директорию /opt, но вы можете выбрать другой вариант (просто замените все директории, указанные в моём руководстве, своими).

После создания учётных записей переместите соответствующие файлы в домашние директории ваших учётных записей.

В моём случае, например, это выглядело следующим образом:
```
/opt/p2poold/p2pool/
/opt/monerod/monerod/
/opt/xmrig/xmrig/
```

Также следует помнить о соответствующих правах, связанных с директориями. Убедитесь в том, что p2pool и monerod обладают всеми необходимыми правами в своей директории (и всем её содержимым).
```
sudo chown -R p2poold:p2poold /opt/p2poold;
sudo chown -R monerod:monerod /opt/monerod;
```

### _Systemd_

Systemd работает с так называемыми файлами сервисов (service files), которые размещаются в директории `/lib/systemd/system/`. Мы используем три из них следующим образом: один для monerod, один для p2pool и один для xmrig.

- /lib/systemd/system/monerod.service

(подразумевает, что пользователь, в случае с monerod, также называется monerod, и путь к файл будет таким же, как у меня)
```
[Unit]
Description=Monerod

[Service]
User=monerod
Group=monerod
ExecStart=/opt/monerod/monerod/monerod --non-interactive --zmq-pub 'tcp://127.0.0.1:18083' --disable-dns-checkpoints --enable-dns-blocklist --limit-rate-down 128 --limit-rate-up 24
Restart=on-failure
RestartSec=5s

[Install]
WantedBy=multi-user.target
```

Для запуска monerod следует использовать следующие команды:
```
sudo systemctl daemon-reload;
sudo systemctl enable monerod;
sudo systemctl start monerod;
```

Первая команда перегружает конфигурацию после изменения файлов сервисов, вторая добавляет monerod в автозапуск, а третья запускает его.

- /lib/systemd/system/p2pool.service
```
[Unit]
Description=P2pool
After=network-online.target systemd-modules-load.service monerod.service
[нечёткое совпадение]After=network-online.target systemd-modules-load.service monerod.service

[Service]
User=p2pool
Group=p2pool
WorkingDirectory=/opt/p2poold/p2pool/
ExecStart=/opt/p2poold/p2pool/p2pool --config mini_config.json --loglevel 2 --p2p 0.0.0.0:37888 --host 127.0.0.1 --stratum-api --wallet "<YOUR_WALLET>"
Restart=on-failure
RestartSec=5s

[Install]
WantedBy=multi-user.target
```

Аналогичные команды:
```
sudo systemctl daemon-reload;
sudo systemctl enable p2pool;
sudo systemctl start p2pool;
    • /lib/systemd/system/xmrig.service
[Unit]
Description=Xmrig
After=network-online.target systemd-modules-load.service p2pool.service
Wants=network-online.target systemd-modules-load.service p2pool.service

[Service]
User=root
Group=root
ExecStart=/opt/xmrig/xmrig/xmrig -o 127.0.0.1:3333
Restart=on-failure
RestartSec=5s

[Install]
WantedBy=multi-user.target
```

Аналогичные команды:
```
sudo systemctl daemon-reload;
sudo systemctl enable xmrig;
sudo systemctl start xmrig;
```

Ну вот, всё практически сделано!

## _Дополнительная информация_

Для проверки статуса сервисов можно использовать команду sudo systemctl status <SERVICE_NAME>.
Для того чтобы прочитать журнал, используйте journalctl:
```
sudo journalctl -u xmrig
```

Лично я использую эту команду с флагами -ae, что позволяет начать с конца записей и видеть их в цвете:
```
sudo journalctl -aeu xmrig
```

## _Примечание_

Если вы найдёте какие-либо ошибки в этом руководстве или же решите указать на мою некомпетентность, напишите мне - я постараюсь всё исправить. Так что ваши отзывы приветствуются.

Приятного майнинга!

---

_Источник: [Autostart mining on P2Pool (with systemd)](https://www.reddit.com/r/MoneroMining/comments/sdegvm/autostart_mining_on_p2pool_with_systemd/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
