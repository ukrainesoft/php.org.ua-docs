---
navigation:
  - function.trader-log10.md: « trader\_log10
  - function.trader-macd.md: trader\_macd »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_ma
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_ma

(PECL trader >= 0.2.0)

trader\_ma — Ковзна середня

### Опис

```methodsynopsis
trader_ma(array $real, int $timePeriod = ?, int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
