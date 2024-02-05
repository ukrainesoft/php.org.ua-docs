---
navigation:
  - function.trader-linearreg-slope.md: « trader\_linearreg\_slope
  - function.trader-ln.md: trader\_ln »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_linearreg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_linearreg

(PECL trader >= 0.2.0)

trader\_linearreg - Лінійна регресія

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
