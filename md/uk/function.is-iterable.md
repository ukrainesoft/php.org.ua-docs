Перевіряє, чи змінна ітерується

-   [« isinteger](function.is-integer.html)
    
-   [ісlong »](function.is-long.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Перевіряє, чи змінна ітерується
    

# ісiterable

(PHP 7> = 7.1.0, PHP 8)

ісiterable — Перевіряє, чи змінна ітерована

### Опис

```methodsynopsis
is_iterable(mixed $value): bool
```

Перевіряє, чи вміст змінної псевдотипу відповідає [iterable](language.types.iterable.html), тобто чи вона або масивом (array), або об'єктом, що реалізує [Traversable](class.traversable.html)

### Список параметрів

`value`

Змінна для перевірки

### Значення, що повертаються

Повертає **`true`**, якщо `value` ітерована або **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **ісiterable()****

```php
<?php

var_dump(is_iterable([1, 2, 3]));  // bool(true)
var_dump(is_iterable(new ArrayIterator([1, 2, 3])));  // bool(true)
var_dump(is_iterable((function () { yield 1; })()));  // bool(true)
var_dump(is_iterable(1));  // bool(false)
var_dump(is_iterable(new stdClass()));  // bool(false)

?>
```

### Дивіться також

-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом