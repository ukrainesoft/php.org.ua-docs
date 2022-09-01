---
navigation:
  - function.trader-bbands.html: « traderbbands
  - function.trader-bop.html: traderbop »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderbeta
---
# traderbeta

(PECL trader >= 0.2.0)

traderbeta — Бета

### Опис

```methodsynopsis
trader_beta(array $real0, array $real1, int $timePeriod = ?): array
```

### Список параметрів

`real0`

Масив, що містить реальні значення.

`real1`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
