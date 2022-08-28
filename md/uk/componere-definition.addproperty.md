Додає властивість

-   [« Componere\\Definition::addConstant](componere-definition.addconstant.html)
    
-   [Componere\\Definition::register »](componere-definition.register.html)
    
-   [PHP Manual](index.html)
    
-   [Componere\\Definition](class.componere-definition.html)
    
-   Додає властивість
    

# ComponereDefinition::addProperty

(Componere 2 >= 2.1.0)

ComponereDefinition::addProperty — Додає властивість

### Опис

```methodsynopsis
public Componere\Definition::addProperty(string $name, Componere\Value $value): Definition
```

Повинен оголосити властивість класу у поточному визначенні

### Список параметрів

`name`

Реєстронезалежне ім'я властивості

`value`

Значення якості за промовчанням

### Значення, що повертаються

Поточне визначення

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо `name` вже оголошено як властивість