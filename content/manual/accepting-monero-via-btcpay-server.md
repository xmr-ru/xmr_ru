---
title: "Как принимать Monero с помощью BTCPay Server"
categories:
  - "Руководства"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

## _Введение_

Одной из задач, возложенных на меня сообществом Monero, стала организация поддержки Monero в BTCPay Server, и я чётко осознал, что из-за ориентированности сервера на Bitcoin соответствующая документация окажется более чем далёкой от идеала, если пытаться применить её к Monero.

Чтобы улучшить ситуацию, я решил «поднять» версию BTCPay Server для собственного пользования и в процессе написал руководство. Надеюсь, оно поможет тем, кто желает принимать к оплате Monero в своих магазинах, принимать пожертвования или каким-то иным образом поразвлечься с BTCPay Server!

В рамках настоящего руководства предполагается, что на вашей машине или VPS установлена Ubuntu 20.04+, но большую часть руководства легко перенести и на другие популярные дистрибутивы Linux.

_Выражаю [Майку Олтофу](https://twitter.com/olthoff) из CoinCards огромную благодарность за помощь и уйму материала, позаимствованную из его руководства по WIP, опубликованного [на GitHub](https://github.com/astupidmoose/Monero-on-BTCPay/blob/main/README.md)._

## _Рекомендуемое оборудование_

- Обрезанный узел (тип узла Monero, используемый по умолчанию с BTCPay Server)1
  - 2+ vCPUs/ядра
  - 4GB+ RAM
  - 100GB+ SSD
    - для развёртывания обрезанного узла Bitcoin требуется ~25GB, а для обрезанного узла Monero ~50GB

## _Зачем использовать BTCPay Server для приёма платежей в Monero?_

Несмотря на существование нескольких вариантов, которыми предприниматели могут воспользоваться, чтобы принимать оплату в Monero, BTCPay Server остаётся одной из лучших опций, благодаря полной суверенности и лёгкости адаптации к другим криптовалютам (таким как Bitcoin или Lightning), а также простоте развёртывания.

Результатом широкой распространённости BTCPay Server также является разнообразный ряд поддерживаемых плагинов для обычных электронных коммерческих платформ, и вы можете даже подключить некоторые невероятные дополнительные функции, такие как автоматический перевод других активов в Monero с помощью SideShift или Fixedfloat.

## _Начальное усиление посредством UFW_

Нам необходимо простым способом усилить защиту системы, настроив с помощью UFW брандмауэр таким образом, чтобы имелся доступ только к тем портам, которые необходимы SSH и BTCPay Server.

Прекрасное руководство, которое научит, как начать пользоваться UFW, можно найти на DigitalOcean.

Введите следующие команды, чтобы добавить некоторые базовые правила UFW, и включите брандмауэр:
```
# Deny all non-explicitly allowed ports
# Deny all non-explicitly allowed ports
sudo ufw default deny incoming
sudo ufw default allow outgoing

# Allow SSH access
sudo ufw allow ssh

# Allow HTTP for LetsEncrypt verification
sudo ufw allow http

# Allow HTTPS for the BTCPay Server UI
sudo ufw allow https

# Enable UFW
sudo ufw enable
```
## _Получение домена для вашего сервера_

Чтобы приступить к использованию BTCPay Server, вам понадобится специальный домен, который вы выберете для себя сами.

Я рекомендую купить домен через [Njalla](https://njal.la/) или 1984.is, заплатить в Bitcoin/Monero, а затем ввести публичный IP-адрес вашей сети/VPS с поддоменом по вашему выбору.

Я, например, использую `btcpay.sethforprivacy.com`.

## _Подготовка к установке BTCPay Server_

Официальную документацию можно найти по следующей ссылке: [Полная установка (для технических специалистов): docs.btcpayserver.org](https://docs.btcpayserver.org/Docker/#full-installation-for-technical-users).

К счастью, в случае с BTCPay Server этот шаг будет предельно простым. Помимо этого, вам будет доступна великолепная документация. Так что вам остаётся лишь получить необходимые для установки BTCPay Server файлы:
```
# Login as root
sudo su -

# Create a folder for BTCPay
mkdir BTCPayServer
cd BTCPayServer

# Clone this repository
git clone https://github.com/btcpayserver/btcpayserver-docker
cd btcpayserver-docker
```
В домашней директории привилегированного пользователя будут созданы необходимые папки, и вы попадёте в директорию, позволяющую конфигурировать BTCPay Server.

## _Конфигурирование BTCPay Server с целью обеспечения поддержки Monero_

В рамках настоящего руководства предполагается, что вы хотите получать платежи в Bitcoin и Monero (поскольку это наиболее частая причина, по которой выбирают BTCPay Server), но вы абсолютно свободно можете использовать «сжатую» конфигурацию, если хотите принимать только Monero.

Чтобы надлежащим образом конфигурировать BTCPay Server, следует использовать так называемые переменные среды, позволяющие задать необходимые опции перед установкой и запуском сервера.

_Не забудьте заменить btcpay.EXAMPLE.com адресом домена, который был указан вами ранее!_
```
# Run btcpay-setup.sh with the right parameters
# Set the custom domain you chose to use
export BTCPAY_HOST="btcpay.EXAMPLE.com"

# Use Bitcoin on mainnet
export NBITCOIN_NETWORK="mainnet"

# Enable Bitcoin support
export BTCPAYGEN_CRYPTO1="btc"

# Enable Monero support
export BTCPAYGEN_CRYPTO2="xmr"

# opt-save-storage-xs (opens new window)will keep around 3 months of blocks (prune BTC for 25 GB)
# opt-add-tor enables Tor support for the UI and Bitcoin node
export BTCPAYGEN_ADDITIONAL_FRAGMENTS="opt-save-storage-xs;opt-add-tor"

# Enable automatic HTTPS reverse proxy + SSL certs via Nginx and LetsEncrypt
export BTCPAYGEN_REVERSEPROXY="nginx"

# Allows you to manage the BTCPay Server install from the web UI, update, etc.
export BTCPAY_ENABLE_SSH=true
```
Только поддержка Monero:
```
# Run btcpay-setup.sh with the right parameters
# Set the custom domain you chose to use
export BTCPAY_HOST="btcpay.EXAMPLE.com"

# Enable Monero support
export BTCPAYGEN_CRYPTO1="xmr"

# opt-save-storage-xs (opens new window)will keep around 3 months of blocks (prune BTC for 25 GB)
# opt-add-tor enables Tor support for the UI and Bitcoin node
export BTCPAYGEN_ADDITIONAL_FRAGMENTS="opt-add-tor"

# Enable automatic HTTPS reverse proxy + SSL certs via Nginx and LetsEncrypt
export BTCPAYGEN_REVERSEPROXY="nginx"

# Allows you to manage the BTCPay Server install from the web UI, update, etc.
export BTCPAY_ENABLE_SSH=true
```

## _Конфигурирование и установка BTCPay Server_

Данный шаг невероятно прост, поскольку скрипт, включённый в репозиторий BTCPay Server, скачает и установит все необходимые пакеты и образы Docker, с помощью которых вы сможете запустить BTCPay Server.

```
. ./btcpay-setup.sh -i
```
Эта команда:
- установит Docker;
- установит Docker-Compose;
- гарантирует, что BTCPay Server запустится после перезагрузки с помощью upstart или systemd;
- задаст переменные среды для использования утилит BTCPay;
- добавит утилиты BTCPay в /usr/bin;
- запустит BTCPay Server.
Если всё пройдёт хорошо, вы найдёте ваш новый BTCPay Server в ранее выбранном домене.

## _Создание учётной записи и магазина_

Прежде всего необходимо создать учётную запись для вашего нового сервера. Настоятельно рекомендуется использовать безопасный адрес электронной почты и надёжный пароль (для этого воспользуйтесь менеджером паролей, подобным Bitwarden). Учётная запись позволит создавать магазины, управлять кошельками и так далее.

*Воспользуйтесь официальной документацией, размещённой по этой ссылке*: [Регистрация учётной записи: docs.btcpayserver.org](https://docs.btcpayserver.org/RegisterAccount/).

Как только учётная запись будет создана, можно создавать магазин, чтобы управлять кошельками, счетами и прочими необходимыми вещами, связанными с этим магазином.

*Соответствующую официальную документацию можно найти здесь*: [Создание магазина: docs.btcpayserver.org](https://docs.btcpayserver.org/CreateStore/).

## _Настройка кошельков Bitcoin и Monero_

### _Конфигурирование выбранного кошелька Bitcoin_

Следующие шаги можно пропустить, если вы собираетесь принимать исключительно Monero!

1. Выбрать Setup Wallet (Настроить кошелёк) и предпочтительные опции кошелька Bitcoin.

![01](/img/manuals/accepting-monero-via-btcpay-server/01.png)

Необходимая официальная документация опубликована по следующей ссылке: [Настройка кошелька: docs.btcpayserver.org](https://docs.btcpayserver.org/WalletSetup/).

### _Создание кошелька Monero только для просмотра с помощью Feather Wallet_

1. Feather Wallet можно скачать здесь: [Feather – бесплатный десктоп-кошелёк Monero](https://featherwallet.org/).
2. Создать новый кошелёк Monero (при наличии уже готового кошелька можно сразу перейти к шагу 3):
  - Выбрать Create new wallet (Создать новый кошелёк).
  ![02](/img/manuals/accepting-monero-via-btcpay-server/02.png)  
  - Сохранить мнемоническую фразу!  
  ![03](/img/manuals/accepting-monero-via-btcpay-server/03.png)  
  - Указать подходящее имя кошелька.  
  ![04](/img/manuals/accepting-monero-via-btcpay-server/04.png)  
  - Установить надёжный пароль кошелька.  
  ![05](/img/manuals/accepting-monero-via-btcpay-server/05.png)  
3. На основе нового кошелька создать кошелёк просмотра, который будет использоваться с BTCPay Server:
  - В верхней строке выбрать Wallet (Кошелёк), а затем View-only (Только для просмотра).
  ![06](/img/manuals/accepting-monero-via-btcpay-server/06.png)  
  - Выбрать Create view-only wallet (Создать кошелёк просмотра).  
  ![07](/img/manuals/accepting-monero-via-btcpay-server/07.png)  
  - Выбрать желаемое имя кошелька просмотра и нажать Save (Сохранить).  
  ![08](/img/manuals/accepting-monero-via-btcpay-server/08.png)  
  - Установить надёжный пароль кошелька просмотра.  
  ![09](/img/manuals/accepting-monero-via-btcpay-server/09.png)  
  - Готово  
  ![10](/img/manuals/accepting-monero-via-btcpay-server/10.png)
4.	Запомнить место, где был сохранён кошелёк просмотра, так как нам понадобится загрузить эти файлы в BTCPay Server при выполнении следующего шага.

### _Добавление нового кошелька просмотра в BTCPay Server_

- Зайти в раздел Settings (Настройки), чтобы сконфигурировать кошелёк Monero.

![11](/img/manuals/accepting-monero-via-btcpay-server/11.png)

- Выбрать опцию Monero, а затем нажать Modify (Изменить) рядом с кошельком.

![12](/img/manuals/accepting-monero-via-btcpay-server/12.png)

- Загрузить файл кошелка просмотра Monero и ключи в соответствии с опциями во вкладке опций кошелька Monero (наряду с паролем, если он был задан).
  - Эти файлы, как правило, сохраняются в пользовательской директории в папке Monero, находящейся в папке wallets (кошельки), то есть `/home/sethforprivacy/Monero/wallets/`.
  ![13](/img/manuals/accepting-monero-via-btcpay-server/13.png)
- Выбрать Enable (Использовать) и нажать Save (Сохранить).

Теперь необходимо подождать, пока узлы Bitcoin и Monero не синхронизируются, после чего всё будет настроено!

_Если вам когда-нибудь понадобится заменить кошелёк Monero на какой-то другой, вы не сможете сделать этого посредством пользовательского интерфейса. Для этого необходимо использовать следующую команду:_
```
docker exec -ti btcpayserver_monero_wallet rm /wallet/* && docker restart btcpayserver_monero_wallet
```
_После ввода команды можно будет загрузить файлы нового кошелька точно так же, как это делалось при начальной настройке._

## _Использование своей версии BTCPay Server_

Благодаря превосходному содержанию документации BTCPay Server, всё то, что было написано в них касательно использования Bitcoin, в равной степени применимо и к Monero:

[Руководство пользователя: docs.btcpayserver.org](https://docs.btcpayserver.org/Guide/)

Теперь, когда пользователю нужно будет оплатить счёт, он сможет выбрать Monero и оплатить товар без использования каких-либо дополнительных иерархических систем или баз данных! Счёт, получаемый клиентами/жертвователями и оплаченный в Monero, будет выглядеть примерно так:

![14](/img/manuals/accepting-monero-via-btcpay-server/14.png)

Если же вы хотите узнать, как будет происходить сам платёж при внесении обычного пожертвования / приобретении товара, то можете попробовать сделать это чуть ниже (не бойтесь, что ваши средства куда-то отправятся, и смело нажимайте, если хотите!):

![15](/img/manuals/accepting-monero-via-btcpay-server/15.png)

## _Как внести с вой вклад в развитие поддержки Monero в BTCPay Server_

Если вы хотите внести свой вклад в развитие поддержки Monero в BTCPay Server, ниже приводятся ссылки на соответствующие репозитории:
- [btcpayserver-docker](https://github.com/btcpayserver/btcpayserver-docker)
  - Особенно этот файл: [monero.yaml](https://github.com/btcpayserver/btcpayserver-docker/blob/master/docker-compose-generator/docker-fragments/monero.yml).
  - Этот файл управляет запуском и управлением контейнеров Monero Docker.
- [dockerfile-deps](https://github.com/btcpayserver/dockerfile-deps)
  - Особенно эта директория: [Monero](https://github.com/btcpayserver/dockerfile-deps/tree/master/Monero)
  - Узел Monero и образы Docker кошелька строятся на основе двух файлов .Dockerfile, а скрипт notifier.sh используется для сообщения о работе BTCPay Server при получении транзакции, соответствующей счёту.

А вот те основные области, которые требуют улучшения:
- Нельзя использовать отдельные кошельки для хранения/использования, только один на сервер.
  - Устранение данного ограничения позволит сделать так, чтобы «родственные» копии BTCPay Server, развёрнутые вашими друзьями/членами семьи/членами сообщества, которым вы доверяете, обеспечивали другим доступ к их магазинам без развёртывания собственных BTCPay Server.
- Нельзя заменить/удалить файлы кошельков/ключей Monero каким-либо образом, кроме как вручную посредством CLI.
  - Усовершенствование данного аспекта упростит переход к использованию новых кошельков, замену кошельков, в которых более нет необходимости, и так далее.
- Приём Monero зависит исключительно от API Kraken.
  - Введение альтернативных API, даже в качестве резервных, с целью сбора данных цены позволит владельцам магазинов принимать платежи в Monero, даже если API Kraken окажется недоступным.

## _Заключение_

Огромное, просто невероятно огромное спасибо всем тем контрибьюторам, кто сделал возможной работу BTCPay Server и продолжает совершенствовать сервер, а также тем, кто помогал развитию проекта финансово.

Такой мощный процессор платежей с надёжной поддержкой Monero — это знаковая победа, и я надеюсь, что ещё больше предпринимателей станут пользоваться BTCPay Server и принимать платежи в Monero (и Bitcoin!) в самом ближайшем будущем.

И, как обычно, если в связи с этим постом у вас возникли вопросы или же вы, будучи предпринимателем, хотели бы получить больше информации о том, как принимать платежи в Monero или пользоваться BTCPay Server, свяжитесь со мной через [Signal, Matrix, Threema или email](https://sethforprivacy.com/about/#how-to-contact-me).

---

_Источник: [Accepting Monero via BTCPay Server](https://sethforprivacy.com/guides/accepting-monero-via-btcpay-server/#contributing-to-monero-support-in-btcpay-server)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
