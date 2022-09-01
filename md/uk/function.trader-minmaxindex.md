---
navigation:
  - function.trader-minmax.html: « traderminmax
  - function.trader-minus-di.html: traderminusdi »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderminmaxindex
---
# traderminmaxindex

(PECL trader >= 0.2.0)

traderminmaxindex — Індекси найнижчих та найвищих значень за вказаний період

### Опис

```methodsynopsis
trader_minmaxindex(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
