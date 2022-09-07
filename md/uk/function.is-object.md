---
navigation:
  - function.is-numeric.md: « isnumeric
  - function.is-real.md: ісreal »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: ісobject
---
# ісobject

(PHP 4, PHP 5, PHP 7, PHP 8)

ісobject — Перевіряє, чи є змінна об'єктом.

### Опис

```methodsynopsis
is_object(mixed $value): bool
```

Перевіряє, чи є змінна об'єктом.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, якщо `value` є об'єктом, або **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер **ісobject()** повертає **`true`** для десеріалізованих об'єктів, які не мають оголошення класу (клас **PHPIncompleteClass**). Раніше поверталося **`false`** |

### Приклади

**Приклад #1 Приклад використання **ісobject()****

```php
<?php
// Объявляем простую функцию, которая возвращает
// Масив из нашего объекта
function get_students($obj)
{
    if (!is_object($obj)) {
        return false;
    }

    return $obj->students;
}

// Создаём новый экземпляр класса
// и заполняем некоторыми значениями

$obj = new stdClass();
$obj->students = array('Kalle', 'Ross', 'Felipe');

var_dump(get_students(null));
var_dump(get_students($obj));
?>
```

### Дивіться також

-   [ісbool()](function.is-bool.md) - Перевіряє, чи є змінна булевою
-   [ісint()](function.is-int.md) - Перевіряє, чи є змінна цілим числом
-   [ісfloat()](function.is-float.md) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісstring()](function.is-string.md) - Перевіряє, чи є змінним рядком
-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
