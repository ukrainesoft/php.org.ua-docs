---
navigation:
  - function.is-double.md: « isdouble
  - function.is-int.md: ісint »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісfloat
---
# ісfloat

(PHP 4, PHP 5, PHP 7, PHP 8)

ісfloat — Перевіряє, чи є змінна числом із плаваючою точкою

### Опис

```methodsynopsis
is_float(mixed $value): bool
```

Перевіряє, чи є змінна числом з плаваючою точкою.

> **Зауваження**
> 
> Щоб перевірити, чи є змінна числом або рядком, що містить число (як поле введення у формі, яке завжди є рядком), використовуйте [ісnumeric()](function.is-numeric.md)

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є змінною типу float, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісfloat()****

```php
var_dump(is_float(27.25));
var_dump(is_float('abc'));
var_dump(is_float(23));
var_dump(is_float(23.5));
var_dump(is_float(1e7));  //Научная нотация
var_dump(is_float(true));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(false)
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [ісbool()](function.is-bool.md) - Перевіряє, чи є змінна булевою
-   [ісint()](function.is-int.md) - Перевіряє, чи є змінна цілим числом
-   [ісnumeric()](function.is-numeric.md) - Перевіряє, чи є змінна числом або рядком, що містить число
-   [ісstring()](function.is-string.md) - Перевіряє, чи є змінним рядком
-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
-   [ісobject()](function.is-object.md) - Перевіряє, чи є змінна об'єктом
