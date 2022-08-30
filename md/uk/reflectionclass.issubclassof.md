Перевіряє, чи клас підкласом

-   [« ReflectionClass::isIterateable](reflectionclass.isiterateable.html)
    
-   [ReflectionClass::isTrait »](reflectionclass.istrait.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Перевіряє, чи клас підкласом
    

# ReflectionClass::isSubclassOf

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isSubclassOf — Перевіряє, чи клас підкласом

### Опис

```methodsynopsis
public ReflectionClass::isSubclassOf(ReflectionClass|string $class): bool
```

Перевіряє, чи клас підкласом зазначеного класу чи реалізує зазначений інтерфейс.

### Список параметрів

`class`

Рядок з ім'ям класу, що перевіряється, або об'єкт класу [ReflectionClass](class.reflectionclass.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.html) - Перевіряє, чи є клас інтерфейсом
-   [ReflectionClass::implementsInterface()](reflectionclass.implementsinterface.html) - Перевіряє, чи реалізується інтерфейс
-   [ісsubclassof()](function.is-subclass-of.html) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
-   [getparentclass()](function.get-parent-class.html) - Повертає ім'я батьківського класу для об'єкта чи класу