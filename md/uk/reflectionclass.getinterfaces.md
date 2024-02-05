---
navigation:
  - reflectionclass.getinterfacenames.md: '« ReflectionClass::getInterfaceNames'
  - reflectionclass.getmethod.md: 'ReflectionClass::getMethod »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getInterfaces'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getInterfaces

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getInterfaces — Повертає інтерфейси

### Опис

```methodsynopsis
public ReflectionClass::getInterfaces(): array
```

Повертає інтерфейси.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив (array) інтерфейсів, у якому ключами є імена інтерфейсів, а значеннями – об'єкти [ReflectionClass](class.reflectionclass.md)

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::getInterfaces()\*\*\*\*

```php
<?php
interface Foo { }

interface Bar { }

class Baz implements Foo, Bar { }

$rc1 = new ReflectionClass("Baz");

print_r($rc1->getInterfaces());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [Foo] => ReflectionClass Object
        (
            [name] => Foo
        )

    [Bar] => ReflectionClass Object
        (
            [name] => Bar
        )

)
```

### Дивіться також

-   [ReflectionClass::getInterfaceNames()](reflectionclass.getinterfacenames.md) \- Повертає імена інтерфейсів
