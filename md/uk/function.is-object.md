---
navigation:
  - function.is-numeric.md: « is\_numeric
  - function.is-real.md: is\_real »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_object

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_object — Перевіряє, чи є змінна об'єкт.

### Опис

```methodsynopsis
is_object(mixed $value): bool
```

Перевіряє, чи є змінна об'єкт.

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Повертає **`true`**, если значение`value` - об'єкт, інакше **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Теперь функция**is\_object()** повертає **`true`** для десеріалізованих об'єктів без визначення класу (клас **\_\_PHP\_Incomplete\_Class**). Раніше поверталося **`false`** |

### Приклади

**Приклад #1 Приклад використання функції** is\_object()\*\*\*\*

```php
<?php

// Объявляем простую функцию, которая возвращает
// массив из объекта
function get_students($obj)
{
    if (!is_object($obj)) {
        return false;
    }

    return $obj->students;
}

// Создаём новый экземпляр класса
// и заполняем значениями

$obj = new stdClass();
$obj->students = array('Келли', 'Росс', 'Филипп');

var_dump(get_students(null));
var_dump(get_students($obj));

?>
```

### Дивіться також

-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
