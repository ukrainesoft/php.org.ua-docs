---
navigation:
  - function.trader-plus-dm.md: « trader\_plus\_dm
  - function.trader-roc.md: trader\_roc »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_ppo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_ppo

(PECL trader >= 0.2.0)

trader\_ppo — Процентний ціновий осцилятор

### Опис

```methodsynopsis
trader_ppo(    array $real,    int $fastPeriod = ?,    int $slowPeriod = ?,    int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastPeriod`

Номер періоду для швидкого ковзного середнього. Допустимі значення від 2 до 100000.

`slowPeriod`

Номер періоду для повільного ковзного середнього. Допустимі значення від 2 до 100000.

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
