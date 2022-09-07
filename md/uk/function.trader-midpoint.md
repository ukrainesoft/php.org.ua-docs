---
navigation:
  - function.trader-mfi.md: « tradermfi
  - function.trader-midprice.md: tradermidprice »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradermidpoint
---
# tradermidpoint

(PECL trader >= 0.2.0)

tradermidpoint - Середина відрізка за період

### Опис

```methodsynopsis
trader_midpoint(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
