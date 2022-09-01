---
navigation:
  - function.trader-minindex.html: « traderminindex
  - function.trader-minmaxindex.html: traderminmaxindex »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderminmax
---
# traderminmax

(PECL trader >= 0.2.0)

traderminmax — найнижчі та найвищі значення за вказаний період

### Опис

```methodsynopsis
trader_minmax(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
