---
navigation:
  - function.trader-avgprice.md: « trader\_avgprice
  - function.trader-beta.md: trader\_beta »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_bbands
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_bbands

(PECL trader >= 0.2.0)

trader\_bbands — Смуги Боллінджера

### Опис

```methodsynopsis
trader_bbands(    array $real,    int $timePeriod = ?,    float $nbDevUp = ?,    float $nbDevDn = ?,    int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`nbDevUp`

Розмножувач для верхньої смуги. Допустимі значення від [TRADER\_REAL\_MIN](trader.constants.md#constant.trader-real-min)до[TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`nbDevDn`

Розмножувач для нижньої смуги. Допустимі значення від [TRADER\_REAL\_MIN](trader.constants.md#constant.trader-real-min)до[TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
