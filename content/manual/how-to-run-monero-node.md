---
title: "Запуск узла Monero (упрощённая версия руководства)"
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

Принимая во внимание [постоянные атаки на сеть Monero](https://sethforprivacy.com/posts/moneros-ongoing-network-attack/), настало время пользователям задуматься о создании [собственных узлов](https://www.monerooutreach.org/monero_best_practices/your_own_node.html).

В этом коротком посте я подробно напишу, как можно без труда запустить узел Monero на сервере Linux, наиболее часто используемой для создания виртуальных приватных серверов (VPS) операционной системы. В качестве дистрибутива Linux я настоятельно рекомендую использовать Debian или Ubuntu. По крайней мере, в рамках данного руководства предполагается, что вы пользуетесь одним из них.

Также в этом руководстве допускается, что вы купили и применили SSH к выбранному вами VPS/хосту. Тем не менее, если вам требуется помощь, чтобы начать, вот несколько хороших ссылок, которые помогут вам:
- [Хостинг сервисов, принимающих Monero](https://www.getmonero.org/community/merchants/#hosting)
    - Возможные опции хостинга VPS при сохранении возможности оплаты в Monero с указанием всех «за» и «против» для каждой такой опции
- [Выделенные серверы Hetzner](https://www.hetzner.com/dedicated-rootserver)
    - Надёжный и недорогой сервер в Германии. Провайдер (пока что!) не принимает Monero, но предлагает широкий выбор быстрых узлов.
- [Простое руководство по развёртыванию Linode](https://www.pragmaticlinux.com/2020/07/setup-a-minimal-debian-10-buster-server-as-a-linode-vps/)
    - Если вы используете Linode, пожалуйста, воспользуйтесь моей [реферальной ссылкой](https://www.linode.com/?r=c956dbb75d14063251557a0e5003efb5ceacc74d), и мы вместе получим соответствующий бонус.

Если вы пользуетесь собственным домашним оборудованием, это руководство в целом касается и вас, если на этом оборудовании установлена Ubuntu/Debian.

## _Рекомендуемые параметры аппаратного обеспечения​_

Полный узел:  
- 2+ vCPU/ядра;
- 4GB+ RAM;
- 175GB+ SSD.

Обрезанный узел _(*)_:
- 2+ vCPU/ядра;
- 4GB+ RAM;
- 75GB+ SSD.

_(*) Вариант с обрезанным узлом позволяет создать собственный узел Monero и не тратить при этом много дискового пространства. Более подробная информация содержится в статье Moneropedia, посвящённой обрезанию._

_**Примечание:** Если у вас есть возможность обеспечить неограниченную пропускную способность, не забудьте увеличить значения ограничения пропускной способности в конфигурационных файлах, что ускорит начальную синхронизацию и повысит общую пропускную способность всей сети Monero.​_

## _Зачем запускать собственный узел Monero?​_

В основе сети Monero лежит распределённая сеть узлов Monero, каждый из которых подтверждает транзакции и транслирует их остальным участникам сети, а также помогает новым узлам просто и быстро синхронизироваться согласно текущему состоянию сети.

Запуск собственного узла Monero помогает не только усилить гарантии своей приватности на сетевом уровне, но также и повысить уровень децентрализации, стабильность и скорость сети Monero.

Каждый узел может реализовывать два разных сервиса, каждый из которых уникальным образом положительно влияет на работу сети:
- одноранговый (p2p) порт (18080 по умолчанию): этот порт позволяет другим узлам сети соединяться с вашим узлом, чтобы скачать блокчейн и отправить вам транзакции, которые прошли валидацию и которых у вас ещё нет. Это также повышает уровень приватности сети, так как узел участвует в трансляции транзакции в соответствии с протоколом [Dandelion++](https://www.monerooutreach.org/stories/dandelion.html);
- порт удаленного вызова процедур (RPC) (18089 по умолчанию с ограниченным доступом): доступ к этому порту (особенно с аргументом публичного узла) позволяет другим пользователям сети, особенно тем, которые используют мобильные кошельки или GUI-кошелёк в «простом» режиме, подключаться к вашему узлу, чтобы синхронизировать свои кошельки, не запуская при этом собственный полный узел локально.

В данном руководстве мною приводятся только те конфигурационные файлы и команды Docker, которые открывают порт p2p, поскольку это ключевым образом помогает сети. Вы можете смело использовать один из указанных ниже конфигурационных файлов с аргументом публичного узла, если вы также хотите, чтобы другие тоже узнали о вашем порте RPC с ограниченным доступом.

Вы можете либо развернуть `monerod` [в виде контейнера Docker](https://sethforprivacy.com/guides/run-a-monero-node/), либо настроить узел посредством systemd и при помощи «официальных» двоичных файлов, указанных ниже.

Развёртывание через Docker имеет несколько ключевых преимуществ, а именно предполагает простую установку, подходящую для разных ОС, и автоматическое обновление через [Watchtower](https://containrrr.dev/watchtower/).

_**Примечание:** Примечание: если вы хотите развернуть узел, но это руководство всё ещё представляется слишком продвинутым для вас, зайдите на [xmrcannon.net](https://xmrcannon.net/). Это отличный ресурс сообщества, где вам создадут узел за некоторую плату в Monero._
​
## _Обновление и установка необходимых пакетов​_

Прежде всего нам потребуется установить несколько инструментов, которые понадобятся нам позже:
```
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install -y ufw gpg wget
```

Затем необходимо установить Docker:
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker $USER
su - $USER
```

_**Примечание:** Эта команда загружает скрипт и запускается из корневой директории Docker. Следует быть уверенным в том, что у вас получится сделать это, и осторожным, если используется персональный компьютер. Если вы не хотите делать этого, следуйте официальной документации по установке, опубликованной в репозитории._

## _Начальное усиление защиты посредством UFW​_

Мы гарантируем простую защиту системы, ограничивая брандмауэр доступом только к тем портам, что необходимы для SSH и `monerod`, используя UFW.

Отличная инструкция, которая поможет начать работу с UFW, опубликована на сайте [DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-setup-a-firewall-with-ufw-on-an-ubuntu-and-debian-cloud-server).

Чтобы добавить некоторые основные правила UFW и включить брандмауэр, выполните следующие команды:
```
# Отключение всех не обозначенных в качестве разрешённых портов
sudo ufw default deny incoming
sudo ufw default allow outgoing

# Открытие доступа SSH
sudo ufw allow ssh

# Открытие доступа к p2p порту monerod
sudo ufw allow 18080/tcp

# Открытие ограниченного доступа к RPC порту monerod
sudo ufw allow 18089/tcp

# Включение UFW
sudo ufw enable
```

## _Загрузка и установка Monero посредством Docker​_

Выберите соответствующий набор команд из приведённых ниже в зависимости от того, хотите ли вы запустить полный узел или обрезанный, а также хотите ли вы, чтобы другие пользователи знали о вашем публичном узле RPC с ограниченным доступом и могли синхронизировать свои кошельки с помощью этого узла:

Альтернативный вариант реализации Docker также можно найти на [GitHub](https://github.com/lalanza808/docker-monero-node). Он даже включает в себя собственные визуальные представления Grafana. Я планировал сделать данное руководство максимально простым, поэтому остановлюсь только на `monerod`.

Если вы хотите проверить исходный код опубликованного здесь образа или написать его самостоятельно, перейдите по ссылкам, которые приведены ниже:

Репозиторий с [исходным кодом](https://github.com/sethforprivacy/simple-monerod-docker) и [образы Docker Hub](https://hub.docker.com/r/sethsimmons/simple-monerod)

_**Примечание:** Рекомендуемые мной команды автоматически отображаются полностью ниже, но по необходимости вы можете выбрать один из трёх других вариантов._

**_Конфигурационный файл monerod Docker c ограниченным доступом к PRC_**

```
docker run -d --restart unless-stopped --name="monerod" -p 18080:18080 -p 18089:18089 -v bitmonero:/home/monero sethsimmons/simple-monerod:latest --rpc-restricted-bind-ip=0.0.0.0 --rpc-restricted-bind-port=18089 --no-igd --no-zmq --enable-dns-blocklist
docker run -d \
    --name watchtower --restart unless-stopped \
    -v /var/run/docker.sock:/var/run/docker.sock \
    containrrr/watchtower --cleanup \
    monerod tor
```

**_Конфигурационный файл monerod Docker с публичным доступом к PRC_**

```
docker run -d --restart unless-stopped --name="monerod" -p 18080:18080 -p 18089:18089 -v bitmonero:/home/monero sethsimmons/simple-monerod:latest --rpc-restricted-bind-ip=0.0.0.0 --rpc-restricted-bind-port=18089 --public-node --no-igd --no-zmq --enable-dns-blocklist
docker run -d \
    --name watchtower --restart unless-stopped \
    -v /var/run/docker.sock:/var/run/docker.sock \
    containrrr/watchtower --cleanup \
    monerod tor
```

**_Конфигурационный файл monerod Docker c ограниченным доступом к PRC (обрезанный узел)_**

```
docker run -d --restart unless-stopped --name="monerod" -p 18080:18080 -p 18089:18089 -v bitmonero:/home/monero sethsimmons/simple-monerod:latest --rpc-restricted-bind-ip=0.0.0.0 --rpc-restricted-bind-port=18089 --no-igd --no-zmq --enable-dns-blocklist --prune-blockchain
docker run -d \
    --name watchtower --restart unless-stopped \
    -v /var/run/docker.sock:/var/run/docker.sock \
    containrrr/watchtower --cleanup \
    monerod tor
```

**_Конфигурационный файл monerod Docker с публичным доступом к PRC (обрезанный узел)_**

```
docker run -d --restart unless-stopped --name="monerod" -p 18080:18080 -p 18089:18089 -v bitmonero:/home/monero sethsimmons/simple-monerod:latest --rpc-restricted-bind-ip=0.0.0.0 --rpc-restricted-bind-port=18089 --public-node --no-igd --no-zmq --enable-dns-blocklist --prune-blockchain
docker run -d \
    --name watchtower --restart unless-stopped \
    -v /var/run/docker.sock:/var/run/docker.sock \
    containrrr/watchtower --cleanup \
    monerod tor
```

Чтобы посмотреть записи журналов для `monerod`, просто введите:
`docker logs --follow monerod`

## _Обновление узла Monero​_

Каждый раз при выходе новой версии вы стараетесь как можно быстрее обновить своё программное обеспечение, чтобы получить самые последние исправления, улучшения и функции.

Загрузите новые двоичные файлы:
```
cd ~
./download_monero_binaries.sh
```

Установите новые двоичные файлы и перезагрузите `monerod`:
```
rm -rf monero-x86_64-linux-gnu-*

tar xvf monero-linux-*.tar.bz2
rm monero-linux-*.tar.bz2
sudo systemctl stop monerod
sudo cp -r monero-x86_64-linux-gnu-*/* /usr/local/bin/
sudo chown -R monero:monero /usr/local/bin/monero*
sudo systemctl start monerod
```

Выполнение этих команд позволит вам скачать самую последнюю версию двоичных файлов, заменить ими старые и перезапустить `monerod` в его новой версии!

## _Передача команд вашему узлу​_

`monerod` поддерживает локальную отправку команд, что позволяет получать дополнительную информацию о статусе `monerod`, задавать ограничения пропускной способности, ограничения для одноранговых узлов и т. д.

Полный список команд, начиная с версии `v0.17.1.8`, можно найти ниже или воспользовавшись `monerod` help:.

**_Вывод команды monerod help_**

```
Monero 'Oxygen Orion' (v0.17.1.8-release)

Commands:
  alt_chain_info [blockhash]
  apropos <keyword> [<keyword> ...]
  ban [<IP>|@<filename>] [<seconds>]
  banned <address>
  bans
  bc_dyn_stats <last_block_count>
  check_blockchain_pruning
  diff
  exit
  flush_cache [bad-txs] [bad-blocks]
  flush_txpool [<txid>]
  hard_fork_info
  help [<command>]
  hide_hr
  in_peers <max_number>
  is_key_image_spent <key_image>
  limit [<kB/s>]
  limit_down [<kB/s>]
  limit_up [<kB/s>]
  mining_status
  out_peers <max_number>
  output_histogram [@<amount>] <min_count> [<max_count>]
  pop_blocks <nblocks>
  print_bc <begin_height> [<end_height>]
  print_block <block_hash> | <block_height>
  print_cn
  print_coinbase_tx_sum <start_height> [<block_count>]
  print_height
  print_net_stats
  print_pl [white] [gray] [pruned] [publicrpc] [<limit>]
  print_pl_stats
  print_pool
  print_pool_sh
  print_pool_stats
  print_status
  print_tx <transaction_hash> [+hex] [+json]
  prune_blockchain
  relay_tx <txid>
  rpc_payments
  save
  set_bootstrap_daemon (auto | none | host[:port] [username] [password])
  set_log <level>|<{+,-,}categories>
  show_hr
  start_mining <addr> [<threads>|auto] [do_background_mining] [ignore_battery]
  status
  stop_daemon
  stop_mining
  sync_info
  unban <address>
  update (check|download)
  version
```

Если вы хотите ввести команду, просто запустите `docker exec monerod/usr/local/bin/monerod name_of_command`, и он автоматически подключится к демону, выполнит команду и распечатает результаты выполнения этой команды в инструменте командной строки.
Вот несколько команд, которые я использую наиболее часто:
- `docker exec monerod /usr/local/bin/monerod status`: получение краткой информации о состоянии `monerod`, включая информацию о количестве пиров (как входящих, так и исходящих), высоте блока, состоянии синхронизации и версии;
- `docker exec monerod /usr/local/bin/monerod sync_info`: отображение списка пиров с информацией об их состоянии и о том, как ваш узел синхронизируется с ними;
- `docker exec monerod /usr/local/bin/monerod print_net_stats`: отображение сетевой статистики с момента запуска `monerod`, включая информацию об общем объёме входящего и исходящего трафика, средней скорости и заданных ограничениях;
- `docker exec monerod /usr/local/bin/monerod update check`: проверка наличия обновлённой версии `monerod`.

## _Перенаправление портов​_

Если вы решите воспользоваться этим руководством, создавая узел на устройстве в своей домашней сети, вам необходимо обязательно перенаправить порты `18080/tcp` и `18089/tcp` посредством маршрутизатора или же [используя анонимную сеть, такую как Tor](https://blog.sethforprivacy.com/guides/run-a-monero-node/#tor).

Хороший основной сайт с множеством руководств по конкретным маршрутизаторам можно найти по адресу [portforward.com](https://portforward.com/router.htm). Просто следует убедиться в том, что вы выбрали правильную марку и модель маршрутизатора, а затем открыть порты 18080/18089, но только для TCP.

## _Использование анонимных сетей​_

### _Tor_

Если вы хотите также открыть доступ к своему RPC порту через Tor в качестве скрытого сервиса (Hidden Service), выполните несколько приведённых ниже команд. Это обеспечивает доступ к вашему порту RPC через Tor, минуя выходные узлы.

- Установка контейнера Docker Tor
```
docker run -d --restart unless-stopped --link monerod:monerod --name tor --volume tor-keys:/var/lib/tor/hidden_service/ goldy/tor-hidden-service
```

- Получение адреса HiddenService
```
docker exec -ti tor onions
```

_**Примечание:** Чтобы проверить возможность подключения, просто зайдите на http://replacewithnewonionaddress:18089/get_info и убедитесь, что текстовый блок был получен вами обратно.​_

## _Подключение к вашему новому удалённому узлу​_

Тут всё будет зависеть от кошелька, выбранного вами для использования. Но обычно это просто подразумевает указание IP-адреса вашего узла (либо вашего домашнего IP-адреса, либо адреса вашего хоста, выделенного VPS) или лукового адреса.

Здесь вы найдёте [пример](https://www.getmonero.org/resources/user-guides/remote_node_gui.html) того, как это сделать, в основном десктоп-кошельке.

## _Несколько полезных CLI инструментов Linux​_

Ниже приведены некоторые из моих любимых инструментов для общего использования CLI под Linux. Надеюсь, они помогут вам в обращении с CLI и позволят более внимательно следить за своим узлом!

- [Oh My Zsh](https://ohmyz.sh/) - Будучи превосходной заменой оболочек bash/sh, Oh My Zsh обеспечивает гораздо лучше выделение информации, усовершенствованные функции и поддерживает автоматические обновления через git.
- [vnstat](https://humdi.net/vnstat/) - Простой CLI инструмент для наблюдения и просмотра показателей использования пропускной способности.
- [htop](https://htop.dev/) - Обеспечивает отличную общую картину использования системных ресурсов процессами и гораздо более читабелен, чем `top`.
- [multitail](https://www.vanheusden.com/multitail/) - Гораздо более полнофункциональный способ просмотра журналов (в частности, имеется возможность просмотра более одного журнала за раз).

## _Заключение​_

Надеюсь, это руководство сделает процесс создания удаленного узла на VPS проще для вас. Также вскоре мною планируется публикация других подобных руководств.

Я использовал команды и информацию, содержащиеся в данном руководстве, чтобы запустить новые удалённые узлы на Linode и Hetzner. Вы можете свободно пользоваться им для синхронизации своего кошелька, добавить его в качестве приоритетного узла и т. д.:
`node-1.sethforprivacy.com:18089` (высокопроизводительный узел на Hetzner, расположенный во Франкфурте, Германия)

Также доступен как HiddenService в сети Tor по адресу:
`rbpgdckle3h3vi4wwwrh75usqtoc5r3alohy7yyx57isynvay63nacyd.onion:18089`

Если у вас есть какие-либо вопросы, если вы считаете, что какой-либо шаг требует дополнительного разъяснения, или же вам нужна помощь в настройке и запуске, вы можете связаться со мной через [Twitter, Matrix или по электронной почте](https://sethforprivacy.com/about/#how-to-contact-me).
