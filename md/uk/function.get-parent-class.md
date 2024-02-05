---
navigation:
  - function.get-object-vars.md: « get\_object\_vars
  - function.interface-exists.md: interface\_exists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_parent\_class
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_parent\_class

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_parent\_class — Повертає ім'я батьківського класу для об'єкта або класу

### Опис

```methodsynopsis
get_parent_class(object|string $object_or_class = ?): string|false
```

Повертає ім'я батьківського класу для об'єкта чи класу.

### Список параметрів

`object_or_class`

Тестований об'єкт чи ім'я класу. Якщо викликається з методу об'єкта, цей параметр не обов'язковий.

### Значення, що повертаються

Повертає ім'я батьківського класу, якщо `object_or_class` — це об'єкт чи ім'я класу.

Повертає **`false`**, якщо об'єкт немає батька або переданого класу з таким ім'ям не існує.

Повертає **`false`**, якщо викликана поза об'єктом без параметра.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`object_or_class` тепер приймає лише об'єкти чи коректні імена класів. |

### Приклади

**Приклад #1 Приклад использования функции**get\_parent\_class()\*\*\*\*

```php
<?php

class Dad {
    function __construct()
    {
    // реализация какой-нибудь логики
    }
}

class Child extends Dad {
    function __construct()
    {
        echo "I'm " , get_parent_class($this) , "'s son\n";
    }
}

class Child2 extends Dad {
    function __construct()
    {
        echo "I'm " , get_parent_class('child2') , "'s son too\n";
    }
}

$foo = new child();
$bar = new child2();

?>
```

Результат виконання наведеного прикладу:

```
I'm Dad's son
I'm Dad's son too
```

### Дивіться також

-   [get\_class()](function.get-class.md) \- Повертає ім'я класу, до якого належить об'єкт
-   [is\_subclass\_of()](function.is-subclass-of.md) \- Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
-   [class\_parents()](function.class-parents.md) \- Повертає список батьківських класів заданого класу
