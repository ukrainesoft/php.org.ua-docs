---
navigation:
  - function.trader-midpoint.md: « tradermidpoint
  - function.trader-min.md: tradermin »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradermidprice
---
# tradermidprice

(PECL trader >= 0.2.0)

tradermidprice — Середня ціна за період

### Опис

```methodsynopsis
trader_midprice(array $high, array $low, int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
