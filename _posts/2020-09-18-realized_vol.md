---
layout: post
title: Волатильность 30/60/90 дней
date: 2021-09-18 13:06:52
tags: Разработка/Статистика/R
excerpt_separator: <!--more-->
---

Расчет 30/60/90 дневной волатильности для сравнения и анализу будущих волнений на рынке.
<!--more-->

30 дней
<img src="https://raw.githubusercontent.com/Ragve-hub/scribble/gh-pages/images/real_30.png" alt="">

30-90 дней
<img src="https://raw.githubusercontent.com/Ragve-hub/scribble/gh-pages/images/real30-real90.png" alt="">

Код

```
library(rusquant)

dateFrom = '2005-01-01'
dateTo = Sys.Date()

SPFB.RTS = getSymbols('@RI', src =
                         'Mfd'
                     , from =
                         dateFrom
                     , auto.assign = F,period='day')

log_RI <- diff(log(SPFB.RTS[,4]), lag=1)
a=na.omit(log_RI)

realized.vol30 <- xts(apply(a,2,runSD,n=30), index(a))*sqrt(252)
realized.vol60 <- xts(apply(a,2,runSD,n=60), index(a))*sqrt(252)
realized.vol90 <- xts(apply(a,2,runSD,n=90), index(a))*sqrt(252)

bb <- as.zoo(realized.vol30-realized.vol90)

plot(realized.vol30-realized.vol90)

plot(realized.vol30)

```
