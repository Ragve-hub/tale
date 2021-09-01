---
title: Программная платформа
date: 2021-07-05 21:06:52
tag: Разработка/Инфраструктура
---

### Мы используем Openquant для разработки, тестирования и исполнения торговых стратегий.

<img src="https://raw.githubusercontent.com/Ragve-hub/scribble/gh-pages/images/oq1.png" alt="">

Программная среда предоставляет базовые функции рисования и визуализации графиков,
которые полезны для того, чтобы понять, что вы закачали правильные данные
для тестирования стратегий, что вы корректно соединились с провайдером данных,
что вы можете послать заявку и получить репорты и т.д. То есть для того,
чтобы понять, что вся ваша инфраструктура вокруг торговой стратегии работает корректно
и можно было разрабатывать/торговать портфели стратегий.

Скачать полноценнную версию с ограничением в 30 дней можно на официальном сайте

[Smartquant Framework](http://www.smartquant.com/)

----------

The quant fund setup is a full institutional infrastructure for a quant fund of any size. It includes integrated development environment (OpenQuant), a production trading environment (QuantTrader), and centralized data management (QuantBase) and data and order routing (QuantRouter). 

<img src="https://raw.githubusercontent.com/Ragve-hub/scribble/gh-pages/images/oq2.png" alt="">

----------
Получение данных и исполнение сделок 
осуществляется через следующих провайдеров:

Alfa Direct, Currenex, DB FIX, Finam Transaq, Genesis, Hotspot, IB, Integral,
IQFeed, Ivory Scorpion, Lightspeed, MBTrading, Nordnet, Open E Cry,
OSL FIX, Plaza II, Quik Fix, SAXO FIX, SmartCom, TT Api Fix.

----------
из ask/bid/middle собираются следующие типы баров:

time -  (sec, min, daily,weekly)

tick - кол-во  тиков внутри бара

vol - общий объем бара

range - (high - low) multiplied by 10000


<img src="https://raw.githubusercontent.com/Ragve-hub/scribble/gh-pages/images/data1.png" alt="">

отдельно формируются:

quotes - bid,ask

marketdepth - изменение стакана

<img src="https://raw.githubusercontent.com/Ragve-hub/scribble/gh-pages/images/data2.png" alt="">


