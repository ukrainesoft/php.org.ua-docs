---
navigation:
  - function.trader-trima.md: « trader\_trima
  - function.trader-tsf.md: trader\_tsf »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_trix
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_trix

(PECL trader >= 0.2.0)

trader\_trix - 1-денна швидкість зміни (ROC) потрійний гладкий EMA

### Опис

```methodsynopsis
trader_trix(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
