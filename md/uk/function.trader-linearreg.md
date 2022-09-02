---
navigation:
  - function.trader-linearreg-slope.md: « traderlinearregslope
  - function.trader-ln.md: traderln »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderlinearreg
---
# traderlinearreg

(PECL trader >= 0.2.0)

traderlinearreg - Лінійна регресія

### Опис

```methodsynopsis
trader_linearreg(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
