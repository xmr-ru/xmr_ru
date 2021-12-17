---
title: "Да будет своп! (теперь и в основной сети)"
date: "2021-05-28"
categories:
  - "Новости"
tags:
  - ""
lead: "Мы публикуем версию 0.7.0 инструмента для совершения XMR-BTC свопов."
pager: true
toc: false
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

Данная версия является патчем версии 0.6.0 и по умолчанию при совершении свопа обращается к главной сети. При работе в главной сети как CLI, так и ASB по умолчанию применяют разумные значения (например, при подключении к узлу, для расчёта комиссии и так далее).

Перед запуском программного обеспечения в главной сети обязательно проверьте приложения и воспользуйтесь флагом --testnet, чтобы переключиться на Bitcoin testnet3 и Monero Stagenet. Имейте в виду, что программное обеспечение всё ещё находится на ранней стадии своего существования, и вы совершаете свопы на свой страх и риск.

Помимо переключения на главную сеть также было добавлено несколько новых функций:
- возможность совершения свопов через Tor;
- возможность пользования журналами json, что упрощает использование инструментов для создания приложений поверх имеющегося программного обеспечения;
- возможность ручного ввода команд восстановления и использования исключительного режима возобновления в ASB.

Подробную информацию можно найти в журналах изменений к версии [0.6.0](https://xmr.ru/redirect.php?url=https://github.com/comit-network/xmr-btc-swap/releases/tag/0.6.0), а также к версии [0.7.0](https://xmr.ru/redirect.php?url=https://github.com/comit-network/xmr-btc-swap/releases/tag/0.7.0).

В том случае если вы уже запускали приложение раньше, рекомендуется удалить старый каталог базы данных перед совершением свопа, так как на пути к переключению на главную сеть было внесено несколько критических изменений. При запуске предыдущей версии будет выведена директория данных, если вы используете флаг --debug.

Наш общедоступный ASB тестовой сети по-прежнему работает на:
```
--seller-addr /dnsaddr/xmr-btc-asb.coblox.tech
--seller-peer-id 12D3KooWCdMKjesXMJz1SiZ7HgotrxuqhQJbP5sgBm2BwP1cqThi
```

Убедитесь, что при подключении к тестовой сети ASB вы используете флаг --testnet, то есть:
```
./swap --testnet buy-xmr --receive-address [YOUR_MONERO_STAGNET_ADDRESS] --seller-addr /dnsaddr/xmr-btc-asb.coblox.tech --seller-peer-id 12D3KooWCdMKjesXMJz1SiZ7HgotrxuqhQJbP5sgBm2BwP1cqThi
```

Если вы используете настройки Tor, вы также можете осуществлять свопы посредством общедоступной демонстрационной версии тестовой сети через Tor:
```
--seller-addr /onion3/pzbmpqsyi2j2za2fwmiognupwozjlcoajbd3cgboetql7ooah63zywqd:9939
--seller-peer-id 12D3KooWCdMKjesXMJz1SiZ7HgotrxuqhQJbP5sgBm2BwP1cqThi
```

Подробную информацию о том, как настроить Tor, можно найти здесь.

---

_Источник: [Farcaster: Community update April](https://www.reddit.com/r/Monero/comments/n258e4/farcaster_community_update_april/)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
