---
navigation:
  - function.trader-kama.html: « traderkama
  - function.trader-linearreg-intercept.html: traderlinearregintercept »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
title: traderlinearregangle
---
# traderlinearregangle

(PECL trader >= 0.2.0)

traderlinearregangle - Лінійний регресійний кут

### Опис

```methodsynopsis
trader_linearreg_angle(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
