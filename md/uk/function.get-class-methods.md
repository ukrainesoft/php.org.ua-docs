Повертає масив імен методів класу

-   [« get\_called\_class](function.get-called-class.html)
    
-   [get\_class\_vars »](function.get-class-vars.html)
    
-   [PHP Manual](index.html)
    
-   [Функции работы с классами и объектами](ref.classobj.html)
    
-   Повертає масив імен методів класу
    

# getclassметодів

(PHP 4, PHP 5, PHP 7, PHP 8)

getclassmethods - Повертає масив імен методів класу

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

| Версия | Описание |
| --- | --- |
|  | Параметр `object_or_class` тепер приймає лише об'єкти чи коректні імена класів. |

### Приклади

**Приклад #1 Приклад використання **getclassmethods()****

```php
<?php

class myclass {
    // конструктор
    function __construct()
    {
        return(true);
    }

    // метод 1
    function myfunc1()
    {
        return(true);
    }

    // метод 2
    function myfunc2()
    {
        return(true);
    }
}

$class_methods = get_class_methods('myclass');
// или
$class_methods = get_class_methods(new myclass());

foreach ($class_methods as $method_name) {
    echo "$method_name\n";
}

?>
```

Результат виконання цього прикладу:

```
myclass
myfunc1
myfunc2
```

### Дивіться також

-   [get\_class()](function.get-class.html) - Повертає ім'я класу, до якого належить об'єкт
-   [get\_class\_vars()](function.get-class-vars.html) - Повертає оголошені за умовчанням властивості класу
-   [get\_object\_vars()](function.get-object-vars.html) - Повертає властивості вказаного об'єкту