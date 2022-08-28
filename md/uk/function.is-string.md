Перевіряє, чи є змінним рядком

-   [« is\_scalar](function.is-scalar.html)
    
-   [isset »](function.isset.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Перевіряє, чи є змінним рядком
    

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
$values = array(false, true, null, 'abc', '23', 23, '23.5', 23.5, '', ' ', '0', 0);
foreach ($values as $value) {
    echo "is_string(";
    var_export($value);
    echo ") = ";
    echo var_dump(is_string($value));
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

-   [is\_float()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_bool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [is\_object()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [is\_array()](function.is-array.html) - Визначає, чи є змінна масивом