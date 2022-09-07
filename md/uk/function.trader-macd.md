---
navigation:
  - function.trader-ma.md: « traderма
  - function.trader-macdext.md: tradermacdext »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradermacd
---
# tradermacd

(PECL trader >= 0.2.0)

tradermacd — Змінна середня збіжність/дивергенція

### Опис

```methodsynopsis
trader_macd(    array $real,    int $fastPeriod = ?,    int $slowPeriod = ?,    int $signalPeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastPeriod`

Номер періоду для швидкого ковзного середнього. Допустимі значення від 2 до 100000.

`slowPeriod`

Номер періоду для повільного ковзного середнього. Допустимі значення від 2 до 100000.

`signalPeriod`

Згладжування сигнальної лінії (номер періоду). Допустимі значення від 1 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
