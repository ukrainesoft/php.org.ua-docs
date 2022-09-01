---
navigation:
  - function.get-resource-type.html: « getresourcetype
  - function.intval.html: intval »
  - index.html: PHP Manual
  - ref.var.html: Функції для роботи зі змінними
title: gettype
---
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

| Версия | Описание |
| --- | --- |
|  | Для закритих ресурсів тепер повертається `'resource (closed)'`. Раніше для закритих ресурсів поверталося `'unknown type'` |

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

-   [getdebugtype()](function.get-debug-type.html) - Повертає ім'я типу змінної у вигляді, що підходить для налагодження
-   [settype()](function.settype.html) - Задає тип змінної
-   [getclass()](function.get-class.html) - Повертає ім'я класу, до якого належить об'єкт
-   [ісarray()](function.is-array.html) - Визначає, чи є змінна масивом
-   [ісbool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [ісcallable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [ісfloat()](function.is-float.html) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.html) - Перевіряє, чи є змінна цілим числом
-   [ісnull()](function.is-null.html) - Перевіряє, чи значення змінної дорівнює null
-   [ісnumeric()](function.is-numeric.html) - Перевіряє, чи є змінна числом чи рядком, що містить число
-   [ісobject()](function.is-object.html) - Перевіряє, чи є змінна об'єктом
-   [ісresource()](function.is-resource.html) - Перевіряє, чи є змінна ресурсом
-   [ісscalar()](function.is-scalar.html) - Перевіряє, чи є змінна скалярним значенням
-   [ісstring()](function.is-string.html) - Перевіряє, чи є змінним рядком
-   [functionexists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   [methodexists()](function.method-exists.html) - Перевіряє, чи існує метод у даному класі
