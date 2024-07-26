---
layout: post
title: Алгоритмическая структура
date: 2022-09-20 21:06:52
tags: Фреймфорк
excerpt_separator: <!--more-->

---


 Описание программных и аппаратных технологий для бесперебойной работы. Размещение серверов в датацентре.

<!--more-->

<img src="https://vector-am.ru/images/oq1.png" alt="">


Фреймворк предоставляет базовые функции рисования и визуализации графиков,
которые полезны для того, чтобы понять, что поступили правильные данные
для тестирования стратегий, что корректно соединились с провайдером данных,
что можно послать заявку и получить репорты и т.д. 


[Smartquant Framework](http://www.smartquant.com/)

----------

Этот сетап могут использовать фонды любых размеров. Он включает в сетя средства разработки (Openquant), среду для исполнения стратегий (QuantTrader), централизованное хранилище данных (QuantBase), и также роутинг ордеров и данных (QuantRouter).

<img src="https://vector-am.ru/images/oq2.png" alt="">
----------

## Получение данных и исполнение сделок осуществляется через следующих провайдеров:

Alfa Direct, Currenex, DB FIX, Finam Transaq, Genesis, Hotspot, IB, Integral,
IQFeed, Ivory Scorpion, Lightspeed, MBTrading, Nordnet, Open E Cry,
OSL FIX, Plaza II, Quik Fix, SAXO FIX, SmartCom, TT Api Fix.

----------

из ask/bid/middle собираются следующие типы баров:

time -  (sec, min, daily,weekly)

tick - кол-во  тиков внутри бара

vol - общий объем бара

range - (high - low) multiplied by 10000

<img src="https://ragve.ru/images/data1.png" alt="">

отдельно формируются:

quotes - bid,ask

marketdepth - изменение стакана

<img src="https://ragve.ru/images/data2.png" alt="">

----------

## Наши сервера размещаются поближе к бирже
 [г.Москва. DataSpace- ЦОД уровня Tier 3](https://www.dataspace.ru)




