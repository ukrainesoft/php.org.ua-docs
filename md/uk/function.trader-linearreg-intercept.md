---
navigation:
  - function.trader-linearreg-angle.md: « trader\_linearreg\_angle
  - function.trader-linearreg-slope.md: trader\_linearreg\_slope »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_linearreg\_intercept
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_linearreg\_intercept

(PECL trader >= 0.2.0)

trader\_linearreg\_intercept - Перехоплення лінійної регресії

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
