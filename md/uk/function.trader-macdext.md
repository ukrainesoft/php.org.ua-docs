---
navigation:
  - function.trader-macd.md: « trader\_macd
  - function.trader-macdfix.md: trader\_macdfix »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_macdext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_macdext

(PECL trader >= 0.2.0)

trader\_macdext - MACD з керованим типом MA

### Опис

```methodsynopsis
trader_macdext(    array $real,    int $fastPeriod = ?,    int $fastMAType = ?,    int $slowPeriod = ?,    int $slowMAType = ?,    int $signalPeriod = ?,    int $signalMAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastPeriod`

Номер періоду для швидкого ковзного середнього. Допустимі значення від 2 до 100000.

`fastMAType`

Тип ковзної середньої для швидкого ковзного середнього. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

`slowPeriod`

Номер періоду для повільного ковзного середнього. Допустимі значення від 2 до 100000.

`slowMAType`

Тип ковзної середньої для повільного ковзного середнього. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

`signalPeriod`

Згладжування сигнальної лінії (номер періоду). Допустимі значення від 1 до 100000.

`signalMAType`

Тип ковзної середньої сигнальної лінії. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
