---
navigation:
  - function.trader-log10.html: « traderlog10
  - function.trader-macd.html: tradermacd »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderма
---
# traderма

(PECL trader >= 0.2.0)

traderma — Ковзна середня

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

Тип ковзної середньої. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
