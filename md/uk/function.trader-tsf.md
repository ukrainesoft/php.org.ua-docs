---
navigation:
  - function.trader-trix.html: « tradertrix
  - function.trader-typprice.html: tradertypprice »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradertsf
---
# tradertsf

(PECL trader >= 0.2.0)

tradertsf - Прогноз тимчасового ряду

### Опис

```methodsynopsis
trader_tsf(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
