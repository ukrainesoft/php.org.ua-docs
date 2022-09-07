---
navigation:
  - function.trader-sinh.md: « tradersinh
  - function.trader-sqrt.md: tradersqrt »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradersma
---
# tradersma

(PECL trader >= 0.2.0)

tradersma — Просте ковзне середнє

### Опис

```methodsynopsis
trader_sma(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
