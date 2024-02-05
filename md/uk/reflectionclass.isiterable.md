---
navigation:
  - reflectionclass.isinternal.md: '« ReflectionClass::isInternal'
  - reflectionclass.isiterateable.md: 'ReflectionClass::isIterateable »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isIterable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isIterable

(PHP 7 >= 7.2.0, PHP 8)

ReflectionClass::isIterable — Перевірити, чи клас ітерується.

### Опис

```methodsynopsis
public ReflectionClass::isIterable(): bool
```

Перевіряє, чи реалізує клас інтерфейс Iterator (тобто можна використовувати його в [foreach](control-structures.foreach.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Использование**ReflectionClass::isIterable()\*\*\*\*

```php
<?php

class IteratorClass implements Iterator {
    public function __construct() { }
    public function key() { }
    public function current() { }
    function next() { }
    function valid() { }
    function rewind() { }
}
class DerivedClass extends IteratorClass { }
class NonIterator { }

function dump_iterable($class) {
    $reflection = new ReflectionClass($class);
    var_dump($reflection->isIterable());
}

$classes = array("ArrayObject", "IteratorClass", "DerivedClass", "NonIterator");

foreach ($classes as $class) {
    echo "Класс $class итерируемый? ";
    dump_iterable($class);
}
?>
```

Результат виконання наведеного прикладу:

```
Класс ArrayObject итерируемый? bool(true)
Класс IteratorClass итерируемый? bool(true)
Класс DerivedClass итерируемый? bool(true)
Класс NonIterator итерируемый? bool(false)
```

### Дивіться також

-   [ReflectionClass::\_\_construct()](reflectionclass.construct.md) \- Створює об'єкт класу ReflectionClass
