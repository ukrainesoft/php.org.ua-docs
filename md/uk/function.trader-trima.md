---
navigation:
  - function.trader-trange.md: « tradertrange
  - function.trader-trix.md: tradertrix »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradertrima
---
# tradertrima

(PECL trader >= 0.2.0)

tradertrima - Трикутна ковзна середня

### Опис

```methodsynopsis
trader_trima(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
