---
navigation:
  - function.get-called-class.md: « get\_called\_class
  - function.get-class-vars.md: get\_class\_vars »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_class\_methods
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_class\_methods

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_class\_methods - Повертає масив імен методів класу

### Опис

```methodsynopsis
get_class_methods(object|string $object_or_class): array
```

Повертає масив імен методів класу.

### Список параметрів

`object_or_class`

Ім'я класу чи об'єкт

### Значення, що повертаються

Повертає масив імен методів, оголошених у класі `object_or_class`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`object_or_class` тепер приймає лише об'єкти чи коректні імена класів. |

### Приклади

**Пример #1 Пример использования**get\_class\_methods()\*\*\*\*

```php
<?php

class myclass {
    // конструктор
    function __construct()
    {
        return(true);
    }

    // метод 1
    function myfunc1()
    {
        return(true);
    }

    // метод 2
    function myfunc2()
    {
        return(true);
    }
}

$class_methods = get_class_methods('myclass');
// или
$class_methods = get_class_methods(new myclass());

foreach ($class_methods as $method_name) {
    echo "$method_name\n";
}

?>
```

Результат виконання наведеного прикладу:

```
__construct
myfunc1
myfunc2
```

### Дивіться також

-   [get\_class()](function.get-class.md) \- Повертає ім'я класу, до якого належить об'єкт
-   [get\_class\_vars()](function.get-class-vars.md) \- Повертає оголошені за умовчанням властивості класу
-   [get\_object\_vars()](function.get-object-vars.md) \- Повертає властивості вказаного об'єкту
