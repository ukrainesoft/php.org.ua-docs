---
navigation:
  - function.trader-max.md: « trader\_max
  - function.trader-medprice.md: trader\_medprice »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_maxindex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_maxindex

(PECL trader >= 0.2.0)

trader\_maxindex - Індекс найбільшого значення за вказаний період

### Опис

```methodsynopsis
trader_maxindex(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
