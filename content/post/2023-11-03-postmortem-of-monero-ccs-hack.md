---
title: "Посмертное вскрытие или анализ взлома системы CCS Monero по графу транзакций"
date: "2023-11-03"
categories:
  - "Новости"
tags:
  - "Взлом"
lead: "Согласно опубликованной 1 сентября 2023 года информации злоумышленник, проведя девять транзакций, опустошил баланс кошелька системы CCS Monero на сумму в 2675,73 XMR."
pager: true
toc: false
sidebar: "right"
widgets:
  - "recent"
  - "taglist"
---

Специалисты компании Moonstone Research решили выяснить, как злоумышленнику удалось вывести эти средства, и пришли к нескольким интересным выводам. **В частности, им удалось достоверно отследить три перевода**. В данном отчёте представлена информация, полученная за первые 24 часа расследования. С течением времени объём информации увеличится.

## _Первые транзакции_

К сожалению, в данном случае не удалось сузить область поиска до задействованных выходов enote, поскольку, по имеющимся данным, злоумышленник тратил средства с другого кошелька. Также, поскольку специалистам не были известны ключ транзакции и адрес назначения для указанных девяти переводов, им пришлось предположить, что любой из выходов enote, сгенерированных при создании первых транзакций вывода средств, мог принадлежать злоумышленнику. Никаких выходов сдачи enote на кошелёк системы CCS Monero при этом не поступало.
Вот те девять транзакций, с которых начался анализ:

![1](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/01.png)  

## _Первый отчёт Crescent Discovery Report_

Девять транзакций были введены в сканер Crescent Discovery с целью получения [отчёта](https://moonstoneresearch.com/products/crescent-discovery-report). Граф нефильтрованных транзакций (который является частью полного отчёта) был беспорядочным из-за количества задействованных выходов enote (18).

![2](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/02.png)

_https://moonstoneresearch.com/blog/assets/2023-11-03_1.html_

После того как были отобраны транзакции с одним совпадающим выходом enote, обнаружилась зацепка: [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58).

![3](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/03.png)

_https://moonstoneresearch.com/blog/assets/2023-11-03_2.html_

Данная транзакция использует семнадцать входящих enote и создаёт одиннадцать исходящих. В кольцах транзакции наблюдается наличие следующих девяти отравленных enote, каждый из которых принадлежит уникальным изначальным транзакциям:

![4](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/04.png)

В силу особенностей такого способа отбора ложных выходов Monero крайне маловероятно, что данная транзакция была создана кем-либо, кроме злоумышленника.

Теперь становятся известны истинные выходы колец 1, 2, 3, 4, 9, 10, 11, 12 и 14. Все девять транзакций принадлежат злоумышленнику. Неизвестно, какие средства были потрачены в кольцах 0, 5, 6, 7, 8, 15, 16, и одним из будущих направлений исследований станет обратный анализ этих колец с целью выявления источников предыдущих транзакций, связанных с этими средствами. Этого не делалось в рамках настоящего первоначального анализа, но соответствующее исследование планируется провести позже. Moonstone Research осуществляет как прямой, так и обратный анализ транзакций.

![5](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/05.png)

Если предположить, что это [транзакция PocketChange](https://moonstoneresearch.com/2023/11/03/Postmortem-of-Monero-CCS-Hack#user-of-monerujo-pocketchange), то это будет означать, что один из одиннадцати исходящих enote ушёл к контрагенту, а десять вернулись в качестве сдачи. Однако, возможно, пользователь отправил средства самому себе, и в этом случае все одиннадцать исходящих enote были бы сдачей.

Существуют и другие пути, по которым могла быть потрачена часть средств из девяти исходных транзакций, но они менее вероятны. Транзакции с несколькими совпадениями — обычное явление, когда нельзя определить, какие именно выходы enote были получены.

![6](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/06.png)

## _Второй отчёт Crescent Discovery Report_

С помощью превосходной зацепки в виде транзакции [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58) был составлен новый [отчёт Crescent Discovery Report](https://moonstoneresearch.com/products/crescent-discovery-report), использующий одиннадцать выходов этой транзакции. В результате появилось два кандидата с более чем одним совпадением:

![7](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/07.png)

Прежде всего, внимание было сфокусировано на транзакции [2c5b4...ad5ec](https://xmrchain.net/tx/2c5b45bf398dcae482019a46fb2d06d334bf4260484dc4857fc35db3689ad5ec), поскольку в ней имелось больше всего совпадений:

![8](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/08.png)

## _Третий и четвёртый отчёты Crescent Discovery Report_

Все кольца, кроме кольца 2, были затронуты. Однако было решено сгенерировать ещё один [отчёт](https://moonstoneresearch.com/products/crescent-discovery-report), указав в качестве исходных транзакций [2c5b4...ad5ec](https://xmrchain.net/tx/2c5b45bf398dcae482019a46fb2d06d334bf4260484dc4857fc35db3689ad5ec) и [06550...ca47b](https://xmrchain.net/tx/06550272cdfa1eea98d288b2d57c272b5c52a2b195b4f808c8c03422a58ca47b), и посмотреть, не появится ли какая-нибудь дополнительная информация в графе транзакций. Конечно же, обнаружилось, что вредоносный enote [8949a...d4277](https://xmrchain.net/tx/8949a7dc5279599fc6beec7e7f9e318fb96d428680da9e41d553731b453d4277) из кольца 2 транзакции [2c5b4...ad5ec](https://xmrchain.net/tx/2c5b45bf398dcae482019a46fb2d06d334bf4260484dc4857fc35db3689ad5ec) была создан в транзакции [06550272cdfa1eea98d288b2d57c272b5c52a2b195b4f808c8c03422a58ca47b](https://xmrchain.net/tx/). Таким образом, были затронуты все семь колец.

Затем был составлен последний [отчёт Crescent Discovery Report](https://moonstoneresearch.com/products/crescent-discovery-report), содержащий анализ взаимосвязи между всеми этими транзакциями.

![9](/img/post/2023-11-03-postmortem-of-monero-ccs-hack/09.png)

_https://moonstoneresearch.com/blog/assets/2023-11-03_3.html_

Этот [четвёртый отчёт](https://moonstoneresearch.com/products/crescent-discovery-report) позволил с высокой точностью отследить три транзакции злоумышленника. Наиболее вероятной представляется следующая схема:

1.	Злоумышленник опустошил кошелёк CCS Monero путём проведения девяти транзакций.
2.	Злоумышленник отправил XMR контрагенту, сервису, бирже или самому себе в транзакции [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58) с использованием Monerujo PocketChange.
3.	Злоумышленник отправил XMR контрагенту, сервису или бирже в транзакции [06550...ca47b](https://xmrchain.net/tx/06550272cdfa1eea98d288b2d57c272b5c52a2b195b4f808c8c03422a58ca47b).
4.	Злоумышленник отправил XMR контрагенту, сервису или бирже в транзакции [2c5b4...ad5ec](https://xmrchain.net/tx/2c5b45bf398dcae482019a46fb2d06d334bf4260484dc4857fc35db3689ad5ec).

## _Пропавшие средства_

Удалось вычислить большинство выходов enote, но некоторые всё же не были учтены. В случае с транзакцией [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58) с одиннадцатью исходящими enote можно чётко найти будущие транзакции для восьми из них. Скорее всего, не был учтён исходящий enote контрагента и два исходящих enote сдачи. Для этих трёх исходящих enote какая-то чёткая привязка отсутствовала. Но ситуация может измениться по мере продвижения исследования.

Пока не представляется возможным вычислить enote 1aec8...fb136, созданный в транзакции [06550...ca47b](https://xmrchain.net/tx/06550272cdfa1eea98d288b2d57c272b5c52a2b195b4f808c8c03422a58ca47b). Вероятно, это исходящий enote для отправителя, и он будет использован позже. Как вариант, это может быть исходящий enote с нулевым значением, хоть это и маловероятно.

Исходящие enote из транзакции [2c5b4...ad5ec](https://xmrchain.net/tx/2c5b45bf398dcae482019a46fb2d06d334bf4260484dc4857fc35db3689ad5ec) пока отследить не получилось.

## _Биржевые депозиты?_

Всем биржам и сервисам Monero следует проверить, не получали ли они следующие транзакции, которые с большой вероятностью были отправлены злоумышленником:

```
bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58
06550272cdfa1eea98d288b2d57c272b5c52a2b195b4f808c8c03422a58ca47b
2c5b45bf398dcae482019a46fb2d06d334bf4260484dc4857fc35db3689ad5ec
```

Если эти транзакции были получены, пожалуйста, свяжитесь с [info@MoonstoneResearch.com](info@MoonstoneResearch.com), чтобы получить консультации относительно дальнейших действий.
Если вы являетесь членом сообщества Monero, пожалуйста, свяжитесь со всеми известными вам представителями бирж, включая мгновенные обменники, и узнайте, поступали или нет на их депозиты средства в этих транзакциях.

## _Возможно, была использована функция PocketChange кошелька Monerujo_

Необычен сам факт того, что пользователь, который в других случаях создавал транзакции ровно с двумя исходящими enote (что нормально для транзакций Monero), создал начальную единую транзакцию с одиннадцатью исходящими enote.

Транзакции с нетипичным количеством исходящих enote создаются по разным причинам, но почти всегда они связаны с каким-то конкретным вариантом использования. Например, транзакции с несколькими исходящими enote могут быть отправлены биржей нескольким своим клиентам, желающим снять средства. Однако транзакции с более чем двумя исходящими enote, как правило, не направляются для внесения средств на депозит биржи или мгновенного обменника, поскольку в подобных случаях предполагается наличие только одного получателя.

Monerujo — это некастодиальный Android-кошелёк Monero. Он имеет функцию [PocketChange](https://xmr.ru/copyright/articles/2023-06-05-monerujos-pocketchange-what-it-is-and-how-it-works/), которая призвана нивелировать один из недостатков Monero путём создания нескольких «карманов» (выходов enote), которые затем можно потратить в нескольких сценариях, не дожидаясь снятия блокировки, которая длится десять блоков Monero. Представителями команды Monerujo данный механизм описывается следующим образом:

> Пока функция [PocketChange] активна, всякий раз, когда вы используете Monerujo для отправки Monero куда бы то ни было, она будет брать большую монету, делить её на части и распределять меньшие монеты по 10 различным карманам. Таким образом, монеты не сольются снова, и вы будете готовы мгновенно потратить деньги, находящиеся во всех этих карманах, без неудобной 20-минутной задержки.

В конце августа 2023 года командой Monerujo было выпущено [обновление](https://www.reddit.com/r/Monerujo/comments/164tklr/weve_released_an_updated_version_of_monerujo_on/) с более сложной версией PocketChange. Транзакция [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58) была проведена 2 сентября 2023 года. Но теперь, вместо постоянно поддерживаемых десяти карманов, версия Monerujo 3.3.8 позволяет создавать от шести до четырнадцати таких карманов.

Специалисты компании Moonstone Research считают, что злоумышленник, скорее всего, является пользователем кошелька Monerujo и использовал функцию PocketChange. В противном случае маловероятно, что он стал бы создавать транзакцию с одиннадцатью исходящими enote. С их точки зрения это наиболее вероятный вариант, независимо от того, использовал ли злоумышленник Monerujo версии 3.3.7 или 3.3.8.

Теоретически транзакция [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58) могла быть платежом, направленным на адреса сразу нескольких соучастников, но в Moonstone Research считают, что это не так из-за объединения enote впоследствии. Если бы в результате проведения этой транзакции соучастники получили бы по одному исходящему enote, тогда не наблюдалось бы того слияния, которое имело место.

Представители Moonstone Research считают, что транзакция [bb77d...d1a58](https://xmrchain.net/tx/bb77d03cae08942f43cccd759ade505a1c9435470a4a2cabfa5e26d2c93d1a58) была отправлена злоумышленником какому-то другому контрагенту. При этом один из одиннадцати исходящих enote ушёл к контрагенту, а десять вернулись в кошелёк. Также возможно, что в данном случае пользователь произвёл транзакцию «вспенивания», хотя достаточно умный человек не стал бы проводить эту операцию с помощью функции PocketChange.

## _Об отслеживании Monero_

Отслеживание Трассировка(Трассировки?) Monero не является детерминированным, как это часто бывает в случае с отслеживанием Bitcoin и Ethereum. Граф транзакций Monero умышленно усложняется, что приводит к ложноположительным результатам и неоднозначности.

Инструменты Moonstone Research подходят для исследования графов транзакций Monero и используют эвристический анализ для отслеживания средств. Результаты такого анализа могут быть ошибочными. Анализ графов транзакций — полезный инструмент, но его следует использовать наряду с другими доказательствами.

## _О компании Moonstone Research_

Moonstone Research — небольшая компания, занимающаяся анализом блокчейна и исследованием трудно отслеживаемых транзакций. Компания специализируется на отслеживании [программ-вымогателей](https://moonstoneresearch.com/specialties/ransomware) и другого незаконного вредоносного программного обеспечения, а также помогает специалистам с соблюдением нормативных требований при проведении дополнительных расследований и составлении отчётов. Moonstone Research можем помочь с возвратом похищенных средств. Обязательно [свяжитесь](info@MoonstoneResearch.com) с ними, если возникнет такая необходимость.

---

_Источник: [Postmortem of Monero CCS Hack: A Transaction Graph Analysis](https://moonstoneresearch.com/2023/11/03/Postmortem-of-Monero-CCS-Hack)_

_Перевод: [Mr. Pickles](https://t.me/v1docq47)_  
_Коррекция: [Kukima](https://t.me/Kukima)_