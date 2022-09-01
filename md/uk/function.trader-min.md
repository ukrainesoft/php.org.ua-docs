---
navigation:
  - function.trader-midprice.html: « tradermidprice
  - function.trader-minindex.html: traderminindex »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
title: tradermin
---
# tradermin

(PECL trader >= 0.2.0)

tradermin — Найменше значення за вказаний період

### Опис

```methodsynopsis
trader_min(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
