---
navigation:
  - function.trader-mult.md: « tradermult
  - function.trader-obv.md: traderobv »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradernatr
---
# tradernatr

(PECL trader >= 0.2.0)

tradernatr - Нормалізований середній істинний діапазон

### Опис

```methodsynopsis
trader_natr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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
