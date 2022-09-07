---
navigation:
  - function.trader-rsi.md: « traderrsi
  - function.trader-sarext.md: tradersarext »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradersar
---
# tradersar

(PECL trader >= 0.2.0)

tradersar - Параболічний SAR

### Опис

```methodsynopsis
trader_sar(    array $high,    array $low,    float $acceleration = ?,    float $maximum = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`acceleration`

Коефіцієнт прискорення використовується максимального значення. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.md#constant.trader-real-max)

`maximum`

Коефіцієнт прискорення Максимальне значення. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.md#constant.trader-real-max)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
