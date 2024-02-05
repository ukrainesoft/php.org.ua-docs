---
navigation:
  - function.get-resource-type.md: « get\_resource\_type
  - function.intval.md: intval »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: gettype
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
-   `"double"`(з історичних причин у разі типу float повертається`"double"`, а не просто`"float"`) .
-   `"string"`
-   `"array"`
-   `"object"`
-   `"resource"`
-   `"resource (closed)"`з PHP 7.2.0
-   `"NULL"`
-   `"unknown type"`

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Для закритих ресурсів тепер повертається `'resource (closed)'`. . Раніше для закритих ресурсів поверталося `'unknown type'` |

### Приклади

**Пример #1 Пример использования**gettype()\*\*\*\*

```php
<?php

$data = array(1, 1., NULL, new stdClass, 'foo');

foreach ($data as $value) {
    echo gettype($value), "\n";
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
integer
double
NULL
object
string
```

### Дивіться також

-   [get\_debug\_type()](function.get-debug-type.md) \- Повертає ім'я типу змінної у вигляді, що підходить для налагодження
-   [settype()](function.settype.md) \- Задає тип змінної
-   [get\_class()](function.get-class.md) \- Повертає ім'я класу, до якого належить об'єкт
-   [is\_array()](function.is-array.md) \- Визначає, чи є змінна масив
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [is\_callable()](function.is-callable.md) \- Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [is\_float()](function.is-float.md) \- Перевіряє, чи є змінна число з плаваючою точкою
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_null()](function.is-null.md) \- Перевіряє, чи значення змінної null дорівнює
-   [is\_numeric()](function.is-numeric.md) \- Перевіряє, чи містить змінне число чи числове рядок
-   [is\_object()](function.is-object.md) \- Перевіряє, чи є змінна об'єкт
-   [is\_resource()](function.is-resource.md) \- Перевіряє, чи є змінна ресурс
-   [is\_scalar()](function.is-scalar.md) \- Перевіряє, чи є змінна скаляр
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   [method\_exists()](function.method-exists.md) \- Перевіряє, чи існує метод у даному класі
