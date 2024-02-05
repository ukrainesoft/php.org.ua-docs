---
navigation:
  - function.is-integer.md: « is\_integer
  - function.is-long.md: is\_long »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_iterable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_iterable

(PHP 7 >= 7.1.0, PHP 8)

is\_iterable — Перевіряє, чи вміст змінної, що ітерується.

### Опис

```methodsynopsis
is_iterable(mixed $value): bool
```

Перевіряє, чи вміст змінної псевдотипу відповідає [iterable](language.types.iterable.md), тобто це або масив (array), або об'єкт, який реалізує інтерфейс [Traversable](class.traversable.md)

### Список параметрів

`value`

Змінна для перевірки.

### Значення, що повертаються

Повертає **`true`**, если значение`value`итерируемо, иначе\*\*`false`\*\*

### Приклади

**Пример #1 Пример использования функции**is\_iterable()\*\*\*\*

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

-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
