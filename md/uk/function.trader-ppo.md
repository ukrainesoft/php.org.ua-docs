---
navigation:
  - function.trader-plus-dm.md: « traderplusдм
  - function.trader-roc.md: traderroc »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderppo
---
# traderppo

(PECL trader >= 0.2.0)

traderppo — Процентний ціновий осцилятор

### Опис

```methodsynopsis
trader_ppo(    array $real,    int $fastPeriod = ?,    int $slowPeriod = ?,    int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastPeriod`

Номер періоду для швидкого ковзного середнього. Допустимі значення від 2 до 100000.

`slowPeriod`

Номер періоду для повільного ковзного середнього. Допустимі значення від 2 до 100000.

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
