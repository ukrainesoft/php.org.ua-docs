---
navigation:
  - function.trader-min.html: « tradermin
  - function.trader-minmax.html: traderminmax »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderminindex
---
# traderminindex

(PECL trader >= 0.2.0)

traderminindex - Індекс найменшого значення за певний період

### Опис

```methodsynopsis
trader_minindex(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
