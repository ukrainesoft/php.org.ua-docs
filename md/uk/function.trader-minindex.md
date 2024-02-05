---
navigation:
  - function.trader-min.md: « trader\_min
  - function.trader-minmax.md: trader\_minmax »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_minindex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_minindex

(PECL trader >= 0.2.0)

trader\_minindex - Індекс найменшого значення за певний період

### Опис

```methodsynopsis
trader_minindex(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
