---
navigation:
  - function.trader-rsi.md: « trader\_rsi
  - function.trader-sarext.md: trader\_sarext »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_sar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_sar

(PECL trader >= 0.2.0)

trader\_sar - Параболічний SAR

### Опис

```methodsynopsis
trader_sar(    array $high,    array $low,    float $acceleration = ?,    float $maximum = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`acceleration`

Коефіцієнт прискорення використовується максимального значення. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`maximum`

Коефіцієнт прискорення Максимальне значення. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
