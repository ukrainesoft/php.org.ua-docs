Перевіряє, чи реалізується інтерфейс

-   [« ReflectionClass::hasProperty](reflectionclass.hasproperty.md)
    
-   [ReflectionClass::inNamespace »](reflectionclass.innamespace.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionClass](class.reflectionclass.md)
    
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

**ReflectionClass::implementsInterface()** викидає [ReflectionException](class.reflectionexception.md), якщо `interface` не є інтерфейсом.

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) - Перевіряє, чи є клас інтерфейсом
-   [ReflectionClass::isSubclassOf()](reflectionclass.issubclassof.md) - Перевіряє, чи є клас підкласом
-   [interfaceexists()](function.interface-exists.html) - Перевіряє, чи визначено інтерфейс
-   [Інтерфейси об'єктів](language.oop5.interfaces.md)