---
title: Боевой сервер
date: 2021-07-04 11:06:52
tag: Разработка/Инфраструктура
---

## Колокейшн

Многие фондовые биржи мира предоставляют услуги colocation клиентам,
желающим разместить свое оборудование в том же дата-центре,
где расположено оборудование биржи, на которой работает её торговая система.

Такая услуга может быть востребована теми, кто желает без посредников напрямую
получать рыночные данные с серверов биржи и/или отправлять свои заявки
в торговую систему биржи. 

Колокейшн подвергается критике за то, что эта услуга якобы дает несправедливое
преимущество одним клиентам биржи над другими, которые отправляют свои заявки
через обычные соединения. Однако по закону услуга колокейшн предоставляется
биржами всем желающим без ограничений при соблюдении определенных требований
к оборудованиюи ежемесячной оплате за услуги. 

Цены на услуги публикуются открыто на сайтах бирж.

Биржи размещают оборудование клиентов в отдельной стойке/стойках, а также строго
следят за тем, чтобы сетевое соединение от всех серверов клиентов до коммутаторов
биржи было строго определенной и одинаковой длины вне зависимости от физического
расстояния от места, где расположен сервер клиента в стойке, до коммутаторов биржи.

Альтернативным и более дешевым вариантом, чем колокейшн, является
proximity hosting - размещение в дата-центре коммуникационной компании, которая напрямую связана
с дата-центром биржи по высокоскоростной линии связи. 

Подобные размещение позволяют минимизировать технологические риски и убытки,
связанные с отключением электричества, интернета, поломкой компьютерного оборудования,
неустойчивой работы терминалов и бирж.


--------------------
В рамках текущей инфраструктуры мы используем QuantTrader - который разработан специально
для развертывания готовых решений в производственной среде.

Исходный код торгуемых стратегии невидим, что обеспечивает более безопасное развертывание
в общих средах, таких как совместное размещение, или в других ситуациях,
когда требуется конфиденциальность.
