---
navigation:
  - function.hypot.md: « hypot
  - function.is-finite.md: is\_finite »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: intdiv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# intdiv

(PHP 7, PHP 8)

intdiv — ділить два числа без залишку

### Опис

```methodsynopsis
intdiv(int $num1, int $num2): int
```

Повертає цілий приватний поділ числа `num1`на число`num2`

### Список параметрів

`num1`

Подільне число, яке потрібно розділити.

`num2`

Дільник, число, на яке ділиться число `num1`

### Значення, що повертаються

Повертає ціле приватне від розподілу числа `num1`на число`num2`

### Помилки

Якщо число `num2` одно , буде викинуто виняток [DivisionByZeroError](class.divisionbyzeroerror.md). Якщо число `num1` дорівнює значенню константи **`PHP_INT_MIN`**, а число`num2` одно `-1`, буде викинуто виняток [ArithmeticError](class.arithmeticerror.md)

### Приклади

**Пример #1 Пример использования функции**intdiv()\*\*\*\*

```php
<?php

var_dump(intdiv(3, 2));
var_dump(intdiv(-3, 2));
var_dump(intdiv(3, -2));
var_dump(intdiv(-3, -2));
var_dump(intdiv(PHP_INT_MAX, PHP_INT_MAX));
var_dump(intdiv(PHP_INT_MIN, PHP_INT_MIN));
var_dump(intdiv(PHP_INT_MIN, -1));
var_dump(intdiv(1, 0));

?>
```

```
int(1)
int(-1)
int(-1)
int(1)
int(1)
int(1)

Fatal error: Uncaught ArithmeticError: Division of PHP_INT_MIN by -1 is not an integer in %s on line 8
Fatal error: Uncaught DivisionByZeroError: Division by zero in %s on line 9
```

### Дивіться також

-   [](language.operators.arithmetic.md)— Розподіл чисел із плаваючою точкою
-   [`%`](language.operators.arithmetic.md)— Цілочисельний модуль
-   [fmod()](function.fmod.md)— Залишок у вигляді числа з плаваючою точкою від розподілу за модулем
