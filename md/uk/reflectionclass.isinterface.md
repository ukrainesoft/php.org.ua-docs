Перевіряє, чи є клас інтерфейсом

-   [« ReflectionClass::isInstantiable](reflectionclass.isinstantiable.html)
    
-   [ReflectionClass::isInternal »](reflectionclass.isinternal.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Перевіряє, чи є клас інтерфейсом
    

# ReflectionClass::isInterface

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isInterface — Перевіряє, чи клас є інтерфейсом

### Опис

```methodsynopsis
public ReflectionClass::isInterface(): bool
```

Перевіряє, чи є клас інтерфейсом чи ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::isInterface()****

```php
<?php
interface SomeInterface {
    public function interfaceMethod();
}

$class = new ReflectionClass('SomeInterface');
var_dump($class->isInterface());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionClass::isInstance()](reflectionclass.isinstance.html) - Перевіряє, чи належить об'єкт класу