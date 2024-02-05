---
navigation:
  - function.trader-midprice.md: « trader\_midprice
  - function.trader-minindex.md: trader\_minindex »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_min
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_min

(PECL trader >= 0.2.0)

trader\_min — Найменше значення за вказаний період

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
