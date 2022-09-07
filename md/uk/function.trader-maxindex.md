---
navigation:
  - function.trader-max.md: « tradermax
  - function.trader-medprice.md: tradermedprice »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
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
