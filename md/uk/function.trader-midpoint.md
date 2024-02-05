---
navigation:
  - function.trader-mfi.md: « trader\_mfi
  - function.trader-midprice.md: trader\_midprice »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_midpoint
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_midpoint

(PECL trader >= 0.2.0)

trader\_midpoint - Середина відрізка за період

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
