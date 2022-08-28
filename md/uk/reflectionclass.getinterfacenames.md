Повертає імена інтерфейсів

-   [« ReflectionClass::getFileName](reflectionclass.getfilename.html)
    
-   [ReflectionClass::getInterfaces »](reflectionclass.getinterfaces.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає імена інтерфейсів
    

# ReflectionClass::getInterfaceNames

(PHP 5> = 5.2.0, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання **ReflectionClass::getInterfaceNames()****

```php
<?php
interface Foo { }

interface Bar { }

class Baz implements Foo, Bar { }

$rc1 = new ReflectionClass("Baz");

print_r($rc1->getInterfaceNames());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Foo
    [1] => Bar
)
```

### Дивіться також

-   [ReflectionClass::getInterfaces()](reflectionclass.getinterfaces.html) - Повертає інтерфейси