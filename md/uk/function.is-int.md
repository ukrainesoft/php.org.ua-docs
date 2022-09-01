---
navigation:
  - function.is-float.html: « isfloat
  - function.is-integer.html: ісinteger »
  - index.html: PHP Manual
  - ref.var.html: Функції для роботи зі змінними
title: ісint
---
# ісint

(PHP 4, PHP 5, PHP 7, PHP 8)

ісint — Перевіряє, чи є змінна цілим числом

### Опис

```methodsynopsis
is_int(mixed $value): bool
```

Перевіряє, чи тип змінної є цілим.

> **Зауваження**
> 
> Щоб перевірити, чи змінна є числом або рядком, що містить число (як поле введення у формі, яке завжди є рядком), використовуйте [ісnumeric()](function.is-numeric.html)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є цілим числом (int), або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісint()****

```php
<?php
$values = array(23, "23", 23.5, "23.5", null, true, false);
foreach ($values as $value) {
    echo "is_int(";
    var_export($value);
    echo ") = ";
    var_dump(is_int($value));
}
?>
```

Результат виконання цього прикладу:

```
is_int(23) = bool(true)
is_int('23') = bool(false)
is_int(23.5) = bool(false)
is_int('23.5') = bool(false)
is_int(NULL) = bool(false)
is_int(true) = bool(false)
is_int(false) = bool(false)
```

### Дивіться також

-   [ісbool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [ісfloat()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісnumeric()](function.is-numeric.html) - Перевіряє, чи є змінна числом або рядком, що містить число
-   [ісstring()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом
-   [ісobject()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
