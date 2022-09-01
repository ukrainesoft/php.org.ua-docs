---
navigation:
  - function.trader-linearreg-intercept.html: « traderlinearregintercept
  - function.trader-linearreg.html: traderlinearreg »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
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
