---
navigation:
  - function.trader-wclprice.md: « trader\_wclprice
  - function.trader-wma.md: trader\_wma »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_willr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_willr

(PECL trader >= 0.2.0)

trader\_will - Відсотковий діапазон Вільямса

### Опис

```methodsynopsis
trader_willr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
