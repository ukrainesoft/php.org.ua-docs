---
navigation:
  - function.trader-midpoint.md: « trader\_midpoint
  - function.trader-min.md: trader\_min »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_midprice
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_midprice

(PECL trader >= 0.2.0)

trader\_midprice — Середня ціна за період

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
