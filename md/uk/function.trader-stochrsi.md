---
navigation:
  - function.trader-stochf.md: « traderstochf
  - function.trader-sub.md: tradersub »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderstochrsi
---
# traderstochrsi

(PECL trader >= 0.2.0)

traderstochrsi - Стохастичний відносний індекс сили

### Опис

```methodsynopsis
trader_stochrsi(    array $real,    int $timePeriod = ?,    int $fastK_Period = ?,    int $fastD_Period = ?,    int $fastD_MAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`fastK_Period`

Тимчасовий період побудови лінії Fast-K. Допустимі значення від 1 до 100000.

`fastD_Period`

Згладжує для створення лінії Fast-D. Допустимі значення від 1 до 100000, зазвичай встановлено значення 3.

`fastD_MAType`

Тип ковзної середньої для Fast-D. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
