Перевіряє, чи реалізується інтерфейс

-   [« ReflectionClass::hasProperty](reflectionclass.hasproperty.html)
    
-   [ReflectionClass::inNamespace »](reflectionclass.innamespace.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Перевіряє, чи реалізується інтерфейс
    

# ReflectionClass::implementsInterface

(PHP 5, PHP 7, PHP 8)

ReflectionClass::implementsInterface — Перевіряє, чи реалізується інтерфейс

### Опис

```methodsynopsis
public ReflectionClass::implementsInterface(ReflectionClass|string $interface): bool
```

Перевіряє, чи реалізує клас зазначений інтерфейс чи ні.

### Список параметрів

`interface`

Ім'я інтерфейсу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**ReflectionClass::implementsInterface()** викидає [ReflectionException](class.reflectionexception.html), якщо `interface` не є інтерфейсом.

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.html) - Перевіряє, чи є клас інтерфейсом
-   [ReflectionClass::isSubclassOf()](reflectionclass.issubclassof.html) - Перевіряє, чи є клас підкласом
-   [interface\_exists()](function.interface-exists.html) - Перевіряє, чи визначено інтерфейс
-   [Интерфейсы объектов](language.oop5.interfaces.html)