---
navigation:
  - function.is-scalar.md: « isscalar
  - function.isset.md: isset »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісstring
---
# ісstring

(PHP 4, PHP 5, PHP 7, PHP 8)

ісstring — Перевіряє, чи є змінним рядком

### Опис

```methodsynopsis
is_string(mixed $value): bool
```

Перевіряє, чи є цей змінний рядком.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є рядком, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісstring()****

```php
<?php
$values = array(false, true, null, 'abc', '23', 23, '23.5', 23.5, '', ' ', '0', 0);
foreach ($values as $value) {
    echo "is_string(";
    var_export($value);
    echo ") = ";
    echo var_dump(is_string($value));
}
?>
```

Результат виконання цього прикладу:

```
is_string(false) = bool(false)
is_string(true) = bool(false)
is_string(NULL) = bool(false)
is_string('abc') = bool(true)
is_string('23') = bool(true)
is_string(23) = bool(false)
is_string('23.5') = bool(true)
is_string(23.5) = bool(false)
is_string('') = bool(true)
is_string(' ') = bool(true)
is_string('0') = bool(true)
is_string(0) = bool(false)
```

### Дивіться також

-   [ісfloat()](function.is-float.md) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.md) - Перевіряє, чи є змінна цілим числом
-   [ісbool()](function.is-bool.md) - Перевіряє, чи є змінна булевою
-   [ісobject()](function.is-object.md) - Перевіряє, чи є змінна об'єктом
-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
