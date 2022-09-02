---
navigation:
  - function.trader-stoch.md: « traderstoch
  - function.trader-stochrsi.md: traderstochrsi »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderstochf
---
# traderstochf

(PECL trader >= 0.2.0)

traderstochf - Швидкий стохастичний осцилятор

### Опис

```methodsynopsis
trader_stochf(    array $high,    array $low,    array $close,    int $fastK_Period = ?,    int $fastD_Period = ?,    int $fastD_MAType = ?): array
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

`fastD_Period`

Згладжує для створення лінії Fast-D. Допустимі значення від 1 до 100000, зазвичай встановлено значення 3.

`fastD_MAType`

Тип ковзної середньої для Fast-D. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
