---
navigation:
  - function.is-callable.md: « is\_callable
  - function.is-double.md: is\_double »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_countable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_countable

(PHP 7 >= 7.3.0, PHP 8)

is\_countable — Перевіряє, чи є зміст змінної лічильне значення

### Опис

```methodsynopsis
is_countable(mixed $value): bool
```

Перевіряє, чи є вміст змінної масив (array) або об'єкт, який реалізує інтерфейс [Countable](class.countable.md)

### Список параметрів

`value`

Значення для перевірки.

### Значення, що повертаються

Повертає **`true`**, если значение`value` лічильне, інакше **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Добавлена функция**is\_countable()** |

### Приклади

**Приклад #1 Приклад використання функції **is\_countable()****

```php
<?php

var_dump(is_countable([1, 2, 3])); // bool(true)
var_dump(is_countable(new ArrayIterator(['foo', 'bar', 'baz']))); // bool(true)
var_dump(is_countable(new ArrayIterator())); // bool(true)
var_dump(is_countable(new stdClass())); // bool(false)
```

### Дивіться також

-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_iterable()](function.is-iterable.md) \- Перевіряє, чи вміст, що ітерується, змінною
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
