Перетворення на рядок

-   [« ReflectionExtension::isTemporary](reflectionextension.istemporary.html)
    
-   [ReflectionFunction »](class.reflectionfunction.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionExtension](class.reflectionextension.html)
    
-   Перетворення на рядок
    

# ReflectionExtension::function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::toString — Перетворення на рядок

### Опис

```methodsynopsis
public ReflectionExtension::__toString(): string
```

Виконує експорт модуля та повертає його у вигляді рядка string. Це те саме, що й виклик [ReflectionExtension::export()](reflectionextension.export.html) з аргументом `return`, рівним **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає експортований модуль у вигляді рядка, так само як [ReflectionExtension::export()](reflectionextension.export.html)

### Дивіться також

-   [ReflectionExtension::construct()](reflectionextension.construct.html) - Створює об'єкт класу ReflectionExtension
-   [ReflectionExtension::export()](reflectionextension.export.html) - Експортує модуль
-   [toString()](language.oop5.magic.html#object.tostring)