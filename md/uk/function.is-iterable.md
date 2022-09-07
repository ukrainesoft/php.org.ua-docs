---
navigation:
  - function.is-integer.md: « isinteger
  - function.is-long.md: ісlong »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісiterable
---
# ісiterable

(PHP 7> = 7.1.0, PHP 8)

ісiterable — Перевіряє, чи змінна ітерована

### Опис

```methodsynopsis
is_iterable(mixed $value): bool
```

Перевіряє, чи вміст змінної псевдотипу відповідає [iterable](language.types.iterable.md), тобто чи вона або масивом (array), або об'єктом, що реалізує [Traversable](class.traversable.md)

### Список параметрів

`value`

Змінна для перевірки

### Значення, що повертаються

Повертає **`true`**, якщо `value` ітерована або **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **ісiterable()****

```php
<?php

var_dump(is_iterable([1, 2, 3]));  // bool(true)
var_dump(is_iterable(new ArrayIterator([1, 2, 3])));  // bool(true)
var_dump(is_iterable((function () { yield 1; })()));  // bool(true)
var_dump(is_iterable(1));  // bool(false)
var_dump(is_iterable(new stdClass()));  // bool(false)

?>
```

### Дивіться також

-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
