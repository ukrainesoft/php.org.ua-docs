---
navigation:
  - function.get-object-vars.md: « getobjectvars
  - function.interface-exists.md: interfaceexists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getparentclass
---
# getparentclass

(PHP 4, PHP 5, PHP 7, PHP 8)

getparentclass — Повертає ім'я батьківського класу для об'єкта або класу

### Опис

```methodsynopsis
get_parent_class(object|string $object_or_class = ?): string|false
```

Повертає ім'я батьківського класу для об'єкта чи класу.

### Список параметрів

`object_or_class`

Тестований об'єкт чи ім'я класу. Якщо викликається з методу об'єкта, цей параметр не обов'язковий.

### Значення, що повертаються

Повертає ім'я батьківського класу, якщо `object_or_class` є об'єктом чи ім'ям класу.

> **Зауваження**
> 
> Якщо об'єкт не має батька або переданого класу з такою назвою не існує, то повертається **`false`**

Якщо функція викликана без параметрів поза об'єктом, ця функція повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `object_or_class` тепер приймає лише об'єкти чи коректні імена класів |

### Приклади

**Приклад #1 Приклад використання **getparentclass()****

```php
<?php

class Dad {
    function __construct()
    {
    // реализация какой-нибудь логики
    }
}

class Child extends Dad {
    function __construct()
    {
        echo "I'm " , get_parent_class($this) , "'s son\n";
    }
}

class Child2 extends Dad {
    function __construct()
    {
        echo "I'm " , get_parent_class('child2') , "'s son too\n";
    }
}

$foo = new child();
$bar = new child2();

?>
```

Результат виконання цього прикладу:

```
I'm Dad's son
I'm Dad's son too
```

### Дивіться також

-   [getclass()](function.get-class.md) - Повертає ім'я класу, до якого належить об'єкт
-   [ісsubclassof()](function.is-subclass-of.md) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
-   [classparents()](function.class-parents.md) - Повертає список батьківських класів заданого класу
