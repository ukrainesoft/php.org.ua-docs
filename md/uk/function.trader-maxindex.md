---
navigation:
  - function.trader-max.html: « tradermax
  - function.trader-medprice.html: tradermedprice »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
title: tradermaxindex
---
# tradermaxindex

(PECL trader >= 0.2.0)

tradermaxindex - Індекс найбільшого значення за вказаний період

### Опис

```methodsynopsis
trader_maxindex(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
