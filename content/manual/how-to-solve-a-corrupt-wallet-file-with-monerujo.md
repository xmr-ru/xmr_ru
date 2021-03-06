---
title: "Как решить проблему с повреждённым файлом кошелька Monerujo"
categories:
  - "Руководства"
thumbnail: "/img/manuals/how-to-solve-a-corrupt-wallet-file-with-monerujo/01.jpeg"
comments: false
authorbox: false
pager: true
toc: true
mathjax: true
sidebar: "right"
---

## _Описание проблемы_

После недавней агрессивной атаки на узлы и последующего выхода версии 0.17 Monero выяснилось, что некоторые пользователи получают повреждённые файлы кошелька. При довольно странных и необычных условиях (поскольку Monerujo является идеально закодированной программой) может случиться так, что вы, когда попытаетесь открыть один из своих кошельков, увидите такое сообщение: _**Connection to node failed! — check username/password** (Не удалось подсоединиться к узлу! Проверьте имя пользователя/пароль)_.

Это не имеет ничего общего ни с соединением, ни с вашим именем пользователя или паролем. У нас есть догадка, согласно которой это связано с тем, что некоторые узлы предоставляют противоречивую информацию, которая при включении в файлы кошелька на вашем телефоне сводит их с ума, так сказать (это технический термин), в результате чего они теряют связь с реальностью и впоследствии не открываются.

Но не бойтесь! Ваши средства в безопасности. Есть простое решение, которое в кратчайшие сроки вернёт вас вместе с вашими любимыми секретными сбережениями в обычное русло.

## _Решение проблемы_

Ваша миссия выполнима, и если вы решитесь на это, то вам просто понадобится сбросить настройки вашего кошелька. Для этого на главном экране выберите меню с тремя точками, расположенное рядом с именем вашего кошелька. Затем выберите _**Reset wallet!** (Сбросить настройки кошелька!)_.

Прочитайте короткое предупреждение. В нём будет сказано, что при сбросе вы потеряете всю имеющуюся информацию, связанную с вашим кошельком, которая не была получена непосредственно из блокчейна Monero. Поскольку файл кошелька был повреждён, Monerujo удалит файл кэша и создаст новый, чтобы вы снова смогли пользоваться своим кошельком. Информация, которую вы потеряете, — это всё то, что было введено вами самостоятельно в процессе использования кошелька, например, заметки о некоторых конкретных транзакциях или имена, которые вы выбирали для своих подадресов или счетов. Все эти подадреса и счета появятся снова, но уже без каких-либо красивых настроек.

Нажмите _**I get it!** (Я понял)_, а затем _**YES DO THAT!** (Выполнить)_.

### _Если это сработает_

Теперь вы можете с видом триумфатора смахнуть со лба пот и считать дело сделанным. Вы теперь практически крутой хакер. Налепите пару памятных наклеек на свой ноутбук и поднимите [стаканчик горячительного](https://en.wikipedia.org/wiki/Club-Mate#Tschunk) за победу.

### _Если это не сработает_

Ну... это уже сложнее. Напишите нам по адресу help@monerujo.io, и мы постараемся устранить возникшие неполадки сообща. Пожалуйста, не удаляйте свой кошелёк, не удаляйте Monerujo. Также не стоит с яростью разбивать свой телефон о стену. Это только усугубит ситуацию.

Также, пожалуйста, помните, что Monerujo был создан очень небольшой группой весёлых пиратов, и это бесплатное программное обеспечение с открытым исходным кодом. Не забывайте вносить свои пожертвования, неблагодарные негодяи (как только ваш кошелёк снова заработает, само собой)!

### _Как избежать этой проблемы в следующий раз_

К сожалению, нельзя полностью исключить возможность повреждения файла вашего кошелька в будущем. Но можно свести к минимуму потерю ценных метаданных при использовании Monero. Для этого следует создать резервную копию файлов вашего кошелька.

Сделать это очень просто. Просто на главном экране вашего кошелька войдите в меню с точками и выберите опцию _**Backup** (Резервное копирование)_. Программа спросит, в какое из хранилищ вашего телефона вы хотите сохранить файл резервной копии. И всё. Monerujo создаст архив zip с файлами вашего кошелька и со всей дополнительной информацией, которая накопилась до момента создания данной резервной копии. И вы можете делать это настолько часто, насколько считаете адекватным и соответствующим ценности ваших метаданных.

В том случае, если вы столкнетесь с той же проблемой (или же захотите проверить, как работает резервное копирование), перейдите в верхнее правое меню на главном экране и найдите опцию _**Import wallet** (Импорт кошелька)_. Опция позволяет создать новый кошелек, который будет называться так же, как ваш старый. И если вы используете то же устройство, кошелёк будет открываться тем же паролем.

Пожалуйста, помните, что файлы вашего кошелька и архив zip с их резервной копией зашифрованы сгенерированным безумным и безопасным паролем, поэтому его следует записать, как и мнемоническую фразу вашего кошелька (так, на всякий случай). Чтобы затем просмотреть их, выберите _**Show secrets!** (Просмотреть секретную информацию)_ в меню кошелька. В результате вы увидите пароль, необходимый для восстановления файлов кошелька (Wallet Files Restore Password). Это официальный пароль шифрования кошелька. Если у вас есть архив zip с резервной копией файлов и этот безумно длинный и сложный пароль, вы будете в состоянии решить невероятное множество всевозможных проблем.

---

_Источник: [How to solve a corrupt wallet file with Monerujo](https://anhdres.medium.com/how-to-solve-a-corrupt-wallet-file-with-monerujo-19fc621b1f2d)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_
