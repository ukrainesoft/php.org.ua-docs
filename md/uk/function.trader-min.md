---
navigation:
  - function.trader-midprice.md: « tradermidprice
  - function.trader-minindex.md: traderminindex »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
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
