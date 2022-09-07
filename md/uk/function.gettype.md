---
navigation:
  - function.get-resource-type.md: « getresourcetype
  - function.intval.md: intval »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
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

$data = array(1, 1., NULL, new stdClass, 'foo');

foreach ($data as $value) {
    echo gettype($value), "\n";
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

-   [getdebugtype()](function.get-debug-type.md) - Повертає ім'я типу змінної у вигляді, що підходить для налагодження
-   [settype()](function.settype.md) - Задає тип змінної
-   [getclass()](function.get-class.md) - Повертає ім'я класу, до якого належить об'єкт
-   [ісarray()](function.is-array.md) - Визначає, чи є змінна масивом
-   [ісbool()](function.is-bool.md) - Перевіряє, чи є змінна булевою
-   [ісcallable()](function.is-callable.md) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [ісfloat()](function.is-float.md) - Перевіряє, чи є змінна числом із плаваючою точкою
-   [ісint()](function.is-int.md) - Перевіряє, чи є змінна цілим числом
-   [ісnull()](function.is-null.md) - Перевіряє, чи значення змінної дорівнює null
-   [ісnumeric()](function.is-numeric.md) - Перевіряє, чи є змінна числом чи рядком, що містить число
-   [ісobject()](function.is-object.md) - Перевіряє, чи є змінна об'єктом
-   [ісresource()](function.is-resource.md) - Перевіряє, чи є змінна ресурсом
-   [ісscalar()](function.is-scalar.md) - Перевіряє, чи є змінна скалярним значенням
-   [ісstring()](function.is-string.md) - Перевіряє, чи є змінним рядком
-   [functionexists()](function.function-exists.md) - Повертає true, якщо вказана функція визначена
-   [methodexists()](function.method-exists.md) - Перевіряє, чи існує метод у даному класі
