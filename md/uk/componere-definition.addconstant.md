Додає константу

-   [« Componere\\Definition::\_\_construct](componere-definition.construct.html)
    
-   [Componere\\Definition::addProperty »](componere-definition.addproperty.html)
    
-   [PHP Manual](index.html)
    
-   [Componere\\Definition](class.componere-definition.html)
    
-   Додає константу
    

# ComponereDefinition::addConstant

(Componere 2 >= 2.1.0)

ComponereDefinition::addConstant — Додає константу

### Опис

```methodsynopsis
public Componere\Definition::addConstant(string $name, Componere\Value $value): Definition
```

Повинен оголосити константу класу у поточному визначенні

### Список параметрів

`name`

Реєстронезалежне ім'я константи

`value`

Значення константи має бути невизначеним (undefined) чи статичним

### Значення, що повертаються

Поточне визначення

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо `name` вже оголошено як константа

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо `value` є статичним

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо `value` є невизначеним