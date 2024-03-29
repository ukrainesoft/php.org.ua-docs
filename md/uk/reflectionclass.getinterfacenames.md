---
navigation:
  - reflectionclass.getfilename.md: '« ReflectionClass::getFileName'
  - reflectionclass.getinterfaces.md: 'ReflectionClass::getInterfaces »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getInterfaceNames'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getInterfaceNames

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ReflectionClass::getInterfaceNames — Повертає імена інтерфейсів

### Опис

```methodsynopsis
public ReflectionClass::getInterfaceNames(): array
```

Повертає імена інтерфейсів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив імен інтерфейсів.

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::getInterfaceNames()\*\*\*\*

```php
<?php
interface Foo { }

interface Bar { }

class Baz implements Foo, Bar { }

$rc1 = new ReflectionClass("Baz");

print_r($rc1->getInterfaceNames());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Foo
    [1] => Bar
)
```

### Дивіться також

-   [ReflectionClass::getInterfaces()](reflectionclass.getinterfaces.md) \- Повертає інтерфейси
