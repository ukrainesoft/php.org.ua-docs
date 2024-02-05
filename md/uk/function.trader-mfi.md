---
navigation:
  - function.trader-medprice.md: « trader\_medprice
  - function.trader-midpoint.md: trader\_midpoint »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_mfi
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_mfi

(PECL trader >= 0.2.0)

trader\_mfi - Індекс грошових потоків

### Опис

```methodsynopsis
trader_mfi(    array $high,    array $low,    array $close,    array $volume,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`volume`

Обсяг торгів, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
