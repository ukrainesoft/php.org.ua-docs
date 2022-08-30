Отримує замикання

-   [« ComponereDefinition::isRegistered](componere-definition.isregistered.html)
    
-   [ComponereDefinition::getClosures »](componere-definition.getclosures.html)
    
-   [PHP Manual](index.md)
    
-   [ComponereDefinition](class.componere-definition.html)
    
-   Отримує замикання
    

# ComponereDefinition::getClosure

(Componere 2 >= 2.1.0)

ComponereDefinition::getClosure — Отримує замикання

### Опис

```methodsynopsis
public Componere\Definition::getClosure(string $name): Closure
```

Повинен повернути замикання для вказаного методу

### Список параметрів

`name`

Реєстронезалежне ім'я методу

### Значення, що повертаються

Замикання прив'язане до коректної області

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `name` не знайдено