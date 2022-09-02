---
navigation:
  - function.trader-linearreg-intercept.md: « traderlinearregintercept
  - function.trader-linearreg.md: traderlinearreg »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderlinearregslope
---
# traderlinearregslope

(PECL trader >= 0.2.0)

traderlinearregslope - Лінійний регресійний нахил

### Опис

```methodsynopsis
trader_linearreg_slope(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
