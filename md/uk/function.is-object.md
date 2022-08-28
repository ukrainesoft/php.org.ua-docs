Перевіряє, чи є змінна об'єктом

-   [« is\_numeric](function.is-numeric.html)
    
-   [is\_real »](function.is-real.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Перевіряє, чи є змінна об'єктом
    

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
// Объявляем простую функцию, которая возвращает
// массив из нашего объекта
function get_students($obj)
{
    if (!is_object($obj)) {
        return false;
    }

    return $obj->students;
}

// Создаём новый экземпляр класса
// и заполняем некоторыми значениями

$obj = new stdClass();
$obj->students = array('Kalle', 'Ross', 'Felipe');

var_dump(get_students(null));
var_dump(get_students($obj));
?>
```

### Дивіться також

-   [is\_bool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_float()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [is\_string()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [is\_array()](function.is-array.html) - Визначає, чи є змінна масивом