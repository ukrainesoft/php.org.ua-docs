Перевірити, чи клас ітерується

-   [« ReflectionClass::isInternal](reflectionclass.isinternal.html)
    
-   [ReflectionClass::isIterateable »](reflectionclass.isiterateable.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Перевірити, чи клас ітерується
    

# ReflectionClass::isIterable

(PHP 7> = 7.2.0, PHP 8)

ReflectionClass::isIterable — Перевірити, чи клас ітерується.

### Опис

```methodsynopsis
public ReflectionClass::isIterable(): bool
```

Перевіряє, чи реалізує клас інтерфейс Iterator (тобто можна використовувати його в [foreach](control-structures.foreach.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Використання **ReflectionClass::isIterable()****

```php
<?php

class IteratorClass implements Iterator {
    public function __construct() { }
    public function key() { }
    public function current() { }
    function next() { }
    function valid() { }
    function rewind() { }
}
class DerivedClass extends IteratorClass { }
class NonIterator { }

function dump_iterable($class) {
    $reflection = new ReflectionClass($class);
    var_dump($reflection->isIterable());
}

$classes = array("ArrayObject", "IteratorClass", "DerivedClass", "NonIterator");

foreach ($classes as $class) {
    echo "Класс $class итерируемый? ";
    dump_iterable($class);
}
?>
```

Результат виконання цього прикладу:

```
Класс ArrayObject итерируемый? bool(true)
Класс IteratorClass итерируемый? bool(true)
Класс DerivedClass итерируемый? bool(true)
Класс NonIterator итерируемый? bool(false)
```

### Дивіться також

-   [ReflectionClass::construct()](reflectionclass.construct.html) - Створює об'єкт класу ReflectionClass