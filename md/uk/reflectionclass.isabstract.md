Перевіряє, чи є клас абстрактним

-   [« ReflectionClass::inNamespace](reflectionclass.innamespace.html)
    
-   [ReflectionClass::isAnonymous »](reflectionclass.isanonymous.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Перевіряє, чи є клас абстрактним
    

# ReflectionClass::isAbstract

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isAbstract — Перевіряє, чи клас є абстрактним

### Опис

```methodsynopsis
public ReflectionClass::isAbstract(): bool
```

Перевіряє, чи клас абстрактним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::isAbstract()****

```php
<?php
class          TestClass { }
abstract class TestAbstractClass { }

$testClass     = new ReflectionClass('TestClass');
$abstractClass = new ReflectionClass('TestAbstractClass');

var_dump($testClass->isAbstract());
var_dump($abstractClass->isAbstract());
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.html) - Перевіряє, чи є клас інтерфейсом
-   [Абстрактні класи](language.oop5.abstract.html)