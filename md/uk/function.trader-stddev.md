---
navigation:
  - function.trader-sqrt.md: « tradersqrt
  - function.trader-stoch.md: traderstoch »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderstddev
---
# traderstddev

(PECL trader >= 0.2.0)

traderstddev - Стандартне відхилення

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
