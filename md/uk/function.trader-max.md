---
navigation:
  - function.trader-mavp.md: « trader\_mavp
  - function.trader-maxindex.md: trader\_maxindex »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_max
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_max

(PECL trader >= 0.2.0)

trader\_max — Найбільше значення за вказаний період

### Опис

```methodsynopsis
trader_max(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
