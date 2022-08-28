Швидкий стохастичний осцилятор

-   [« trader\_stoch](function.trader-stoch.html)
    
-   [trader\_stochrsi »](function.trader-stochrsi.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Швидкий стохастичний осцилятор
    

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

Тип ковзної середньої для Fast-D. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.html)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.