Перевіряє, чи клас остаточним (final)

-   [« ReflectionClass::isEnum](reflectionclass.isenum.md)
    
-   [ReflectionClass::isInstance »](reflectionclass.isinstance.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionClass](class.reflectionclass.md)
    
-   Перевіряє, чи клас остаточним (final)
    

# ReflectionClass::isFinal

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isFinal — Перевіряє, чи є клас остаточним (final)

### Опис

```methodsynopsis
public ReflectionClass::isFinal(): bool
```

Перевіряє, чи клас остаточним (final).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::isFinal()****

```php
<?php
class       TestClass { }
final class TestFinalClass { }

$normalClass = new ReflectionClass('TestClass');
$finalClass  = new ReflectionClass('TestFinalClass');

var_dump($normalClass->isFinal());
var_dump($finalClass->isFinal());

?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::isAbstract()](reflectionclass.isabstract.md) - Перевіряє, чи є клас абстрактним
-   [Ключевое слово "final"](language.oop5.final.md)