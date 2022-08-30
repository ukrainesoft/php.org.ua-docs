Перевірити, що вміст змінної є лічильним значенням

-   [« iscallable](function.is-callable.html)
    
-   [ісdouble »](function.is-double.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Перевірити, що вміст змінної є лічильним значенням
    

# ісcountable

(PHP 7> = 7.3.0, PHP 8)

ісcountable — Перевірити, що вміст змінної є лічильним значенням

### Опис

```methodsynopsis
is_countable(mixed $value): bool
```

Перевірити, чи вміст змінної масив (array) або об'єкт, що реалізує [Countable](class.countable.html)

### Список параметрів

`value`

Значення для перевірки

### Значення, що повертаються

Повертає **`true`**, якщо `value` лічильна або **`false`** в іншому випадку.

### список змін

| Версия | Описание                         |
|--------|----------------------------------|
|        | Додана функція **ісcountable()** |

### Приклади

**Приклад #1 Приклади використання **ісcountable()****

```php
<?php
var_dump(is_countable([1, 2, 3])); // bool(true)
var_dump(is_countable(new ArrayIterator(['foo', 'bar', 'baz']))); // bool(true)
var_dump(is_countable(new ArrayIterator())); // bool(true)
var_dump(is_countable(new stdClass())); // bool(false)
```

### Дивіться також

-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом
-   [ісobject()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [ісiterable()](function.is-iterable.html) - Перевіряє, чи є змінна, що ітерується.
-   [ісbool()](function.is-bool.html) - Перевіряє, чи є змінна булевою