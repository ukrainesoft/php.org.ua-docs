---
navigation:
  - function.trader-avgprice.md: « traderavgprice
  - function.trader-beta.md: traderbeta »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderbbands
---
# traderbbands

(PECL trader >= 0.2.0)

traderbbands — Смуги Боллінджера

### Опис

```methodsynopsis
trader_bbands(    array $real,    int $timePeriod = ?,    float $nbDevUp = ?,    float $nbDevDn = ?,    int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`nbDevUp`

Розмножувач для верхньої смуги. Допустимі значення від [TRADERREALMIN](trader.constants.md#constant.trader-real-min) до [TRADERREALMAX](trader.constants.md#constant.trader-real-max)

`nbDevDn`

Розмножувач для нижньої смуги. Допустимі значення від [TRADERREALMIN](trader.constants.md#constant.trader-real-min) до [TRADERREALMAX](trader.constants.md#constant.trader-real-max)

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
