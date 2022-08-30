Отримує прапори поведінки

-   [« ArrayObject::getArrayCopy](arrayobject.getarraycopy.md)
    
-   [ArrayObject::getIterator »](arrayobject.getiterator.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayObject](class.arrayobject.md)
    
-   Отримує прапори поведінки
    

# ArrayObject::getFlags

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ArrayObject::getFlags — Отримує прапори поведінки

### Опис

```methodsynopsis
public ArrayObject::getFlags(): int
```

Отримує прапори поведінки [ArrayObject](class.arrayobject.md). Дивіться метод [ArrayObject::setFlags](arrayobject.setflags.md) Щоб переглянути список можливих прапорів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає прапори поведінки ArrayObject.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getFlags()****

```php
<?php
// Масив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Получение текущих флагов
$flags = $fruitsArrayObject->getFlags();
var_dump($flags);

// Установка новых флагов
$fruitsArrayObject->setFlags(ArrayObject::ARRAY_AS_PROPS);

// Получение новых флагов
$flags = $fruitsArrayObject->getFlags();
var_dump($flags);
?>
```

Результат виконання цього прикладу:

```
int(0)
int(2)
```

### Дивіться також

-   Метод [ArrayObject::setFlags()](arrayobject.setflags.md) - Встановлює прапори поведінки