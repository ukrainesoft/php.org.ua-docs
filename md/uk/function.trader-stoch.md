- [«trader_stddev](function.trader-stddev.md)
- [trader_stochf»](function.trader-stochf.md)

- [PHP Manual](index.md)
- [Функції Trader](ref.trader.md)
- Стохастичний осцилятор

# trader_stoch

(PECL trader \>= 0.2.0)

trader_stoch - Стохастичний осцилятор

### Опис

**trader_stoch**(
array `$high`,
array `$low`,
array `$close`,
int `$fastK_Period` = ?,
int `$slowK_Period` = ?,
int `$slowK_MAType` = ?,
int `$slowD_Period` = ?,
int `$slowD_MAType` = ?
): array

### Список параметрів

`high`
Висока вартість, масив реальних значень.

`low`
Низька вартість, масив реальних значень.

`close`
Ціна закриття, масив реальних значень.

`fastK_Period`
Тимчасовий період побудови лінії Fast-K. Допустимі значення від 1 до
100 000.

`slowK_Period`
Згладжує для створення лінії Slow-K. Допустимі значення від 1 до
100000 зазвичай встановлено значення 3.

`slowK_MAType`
Тип ковзної середньої для Slow-K. Слід використовувати серію констант
[TRADER_MA_TYPE\_\*](trader.constants.md).

`slowD_Period`
Згладжує для створення лінії Slow-D. Допустимі значення від 1 до
100 000.

`slowD_MAType`
Тип ковзної середньої для Slow-D. Слід використовувати серію констант
[TRADER_MA_TYPE\_\*](trader.constants.md).

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі
виникнення помилки.
