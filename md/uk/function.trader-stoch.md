---
navigation:
  - function.trader-stddev.md: « traderstddev
  - function.trader-stochf.md: traderstochf »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderstoch
---
# traderstoch

(PECL trader >= 0.2.0)

traderstoch - Стохастичний осцилятор

### Опис

```methodsynopsis
trader_stoch(    array $high,    array $low,    array $close,    int $fastK_Period = ?,    int $slowK_Period = ?,    int $slowK_MAType = ?,    int $slowD_Period = ?,    int $slowD_MAType = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`fastK_Period`

Тимчасовий період побудови лінії Fast-K. Допустимі значення від 1 до 100000.

`slowK_Period`

Згладжує для створення лінії Slow-K. Допустимі значення від 1 до 100000, зазвичай встановлено значення 3.

`slowK_MAType`

Тип ковзної середньої для Slow-K. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

`slowD_Period`

Згладжує для створення лінії Slow-D. Допустимі значення від 1 до 100000.

`slowD_MAType`

Тип ковзної середньої для Slow-D. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
