Повертає тип змінної

-   [« get\_resource\_type](function.get-resource-type.html)
    
-   [intval »](function.intval.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Повертає тип змінної
    

# gettype

(PHP 4, PHP 5, PHP 7, PHP 8)

gettype — Повертає тип змінної

### Опис

```methodsynopsis
gettype(mixed $value): string
```

Повертає тип PHP-змінної `value`. Для перевірки типу змінної використовуйте функції `is_*`

### Список параметрів

`value`

Перевірена змінна.

### Значення, що повертаються

Можливими значеннями рядка, що повертається, є:

-   `"boolean"`
-   `"integer"`
-   `"double"` (з історичних причин у разі типу float повертається `"double"`, а не просто `"float"`
-   `"string"`
-   `"array"`
-   `"object"`
-   `"resource"`
-   `"resource (closed)"` з PHP 7.2.0
-   `"NULL"`
-   `"unknown type"`

### список змін

| Версия | Описание                                                                                                                  |
|--------|---------------------------------------------------------------------------------------------------------------------------|
|        | Для закритих ресурсів тепер повертається `'resource (closed)'`. Раніше для закритих ресурсів поверталося `'unknown type'` |

### Приклади

**Приклад #1 Приклад використання **gettype()****

```php
<?php

$data = array(1, 1., NULL, new stdClass, 'foo');

foreach ($data as $value) {
    echo gettype($value), "\n";
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
integer
double
NULL
object
string
```

### Дивіться також

-   [get\_debug\_type()](function.get-debug-type.html) - Повертає ім'я типу змінної у вигляді, що підходить для налагодження
-   [settype()](function.settype.html) - Задає тип змінної
-   [get\_class()](function.get-class.html) - Повертає ім'я класу, до якого належить об'єкт
-   [is\_array()](function.is-array.html) - Визначає, чи є змінна масивом
-   [is\_bool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [is\_callable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [is\_float()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [is\_int()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [is\_null()](function.is-null.html) - Перевіряє, чи значення змінної дорівнює null
-   [is\_numeric()](function.is-numeric.html) - Перевіряє, чи є змінна числом чи рядком, що містить число
-   [is\_object()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [is\_resource()](function.is-resource.html) - Перевіряє, чи є змінна ресурсом
-   [is\_scalar()](function.is-scalar.html) - Перевіряє, чи є змінна скалярним значенням
-   [is\_string()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [function\_exists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   [method\_exists()](function.method-exists.html) - Перевіряє, чи існує метод у даному класі