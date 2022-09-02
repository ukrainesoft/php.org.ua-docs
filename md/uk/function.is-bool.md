---
navigation:
  - function.is-array.md: « isarray
  - function.is-callable.md: ісcallable »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісbool
---
# ісbool

(PHP 4, PHP 5, PHP 7, PHP 8)

ісbool — Перевіряє, чи є змінна булевою

### Опис

```methodsynopsis
is_bool(mixed $value): bool
```

Перевіряє, чи є ця змінна булевою.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є змінною типу bool, або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісbool()****

```php
<?php
$a = false;
$b = 0;

// Так как $a является булевой переменной, функция вернёт true
if (is_bool($a) === true) {
    echo "Да, это булевая переменная";
}

// Так как $b не является булевой переменной, функция вернёт false
if (is_bool($b) === false) {
    echo "Нет, это не булевая переменная";
}
?>
```

### Дивіться також

-   [ісfloat()](function.is-float.md) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.md) - Перевіряє, чи є змінна цілим числом
-   [ісstring()](function.is-string.md) - Перевіряє, чи є змінним рядком
-   [ісobject()](function.is-object.md) - Перевіряє, чи є змінна об'єктом
-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
