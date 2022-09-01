---
navigation:
  - function.trader-linearreg-angle.html: « traderlinearregangle
  - function.trader-linearreg-slope.html: traderlinearregslope »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderlinearregintercept
---
# traderlinearregintercept

(PECL trader >= 0.2.0)

traderlinearregintercept - Перехоплення лінійної регресії

### Опис

```methodsynopsis
trader_linearreg_intercept(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
