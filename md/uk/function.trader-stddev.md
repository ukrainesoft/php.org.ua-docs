---
navigation:
  - function.trader-sqrt.md: « trader\_sqrt
  - function.trader-stoch.md: trader\_stoch »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_stddev
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_stddev

(PECL trader >= 0.2.0)

trader\_stddev - Стандартне відхилення

### Опис

```methodsynopsis
trader_stddev(array $real, int $timePeriod = ?, float $nbDev = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`nbDev`

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
