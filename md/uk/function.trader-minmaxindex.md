---
navigation:
  - function.trader-minmax.md: « trader\_minmax
  - function.trader-minus-di.md: trader\_minus\_di »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_minmaxindex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_minmaxindex

(PECL trader >= 0.2.0)

trader\_minmaxindex — Індекси найнижчих та найвищих значень за вказаний період

### Опис

```methodsynopsis
trader_minmaxindex(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
