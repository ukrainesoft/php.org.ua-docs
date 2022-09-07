---
navigation:
  - function.is-callable.md: « iscallable
  - function.is-double.md: ісdouble »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісcountable
---
# ісcountable

(PHP 7> = 7.3.0, PHP 8)

ісcountable — Перевірити, що вміст змінної є лічильним значенням

### Опис

```methodsynopsis
is_countable(mixed $value): bool
```

Перевірити, чи вміст змінної масив (array) або об'єкт, що реалізує [Countable](class.countable.md)

### Список параметрів

`value`

Значення для перевірки

### Значення, що повертаються

Повертає **`true`**, якщо `value` лічильна або **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додана функція **ісcountable()** |

### Приклади

**Приклад #1 Приклади використання **ісcountable()****

```php
<?php
var_dump(is_countable([1, 2, 3])); // bool(true)
var_dump(is_countable(new ArrayIterator(['foo', 'bar', 'baz']))); // bool(true)
var_dump(is_countable(new ArrayIterator())); // bool(true)
var_dump(is_countable(new stdClass())); // bool(false)
```

### Дивіться також

-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
-   [ісobject()](function.is-object.md) - Перевіряє, чи є змінна об'єктом
-   [ісiterable()](function.is-iterable.md) - Перевіряє, чи є змінна, що ітерується.
-   [ісbool()](function.is-bool.md) - Перевіряє, чи є змінна булевою
