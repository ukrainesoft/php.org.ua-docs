---
navigation:
  - reflectionclass.isinstance.md: '« ReflectionClass::isInstance'
  - reflectionclass.isinterface.md: 'ReflectionClass::isInterface »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isInstantiable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isInstantiable

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isInstantiable — Перевіряє, чи можна створити екземпляр класу

### Опис

```methodsynopsis
public ReflectionClass::isInstantiable(): bool
```

Перевіряє, чи можна створити екземпляр класу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::isInstantiable()\*\*\*\*

```php
<?php
class C { }

interface iface {
    function f1();
}

class ifaceImpl implements iface {
    function f1() {}
}

abstract class abstractClass {
    function f1() { }
    abstract function f2();
}

class D extends abstractClass {
    function f2() { }
}

trait T {
    function f1() {}
}

class privateConstructor {
    private function __construct() { }
}

$classes = array(
    "C",
    "iface",
    "ifaceImpl",
    "abstractClass",
    "D",
    "T",
    "privateConstructor",
);

foreach($classes  as $class ) {
    $reflectionClass = new ReflectionClass($class);
    echo "Можно ли создать экземпляр класса $class?  ";
    var_dump($reflectionClass->isInstantiable());
}

?>
```

Результат виконання наведеного прикладу:

```
Можно ли создать экземпляр класса C?  bool(true)
Можно ли создать экземпляр класса iface?  bool(false)
Можно ли создать экземпляр класса ifaceImpl?  bool(true)
Можно ли создать экземпляр класса abstractClass?  bool(false)
Можно ли создать экземпляр класса D?  bool(true)
Можно ли создать экземпляр класса T?  bool(false)
Можно ли создать экземпляр класса privateConstructor?  bool(false)
```

### Дивіться також

-   [ReflectionClass::isInstance()](reflectionclass.isinstance.md) \- Перевіряє, чи належить об'єкт класу
