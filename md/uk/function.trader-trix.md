---
navigation:
  - function.trader-trima.md: « tradertrima
  - function.trader-tsf.md: tradertsf »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradertrix
---
# tradertrix

(PECL trader >= 0.2.0)

tradertrix - 1-денна швидкість зміни (ROC) потрійний гладкий EMA

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
