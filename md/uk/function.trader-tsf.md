---
navigation:
  - function.trader-trix.md: « trader\_trix
  - function.trader-typprice.md: trader\_typprice »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_tsf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_tsf

(PECL trader >= 0.2.0)

trader\_tsf - Прогноз тимчасового ряду

### Опис

```methodsynopsis
trader_tsf(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
