---
navigation:
  - componere-definition.addconstant.html: '« ComponereDefinition::addConstant'
  - componere-definition.register.html: 'ComponereDefinition::register »'
  - index.html: PHP Manual
  - class.componere-definition.html: ComponereDefinition
title: 'ComponereDefinition::addProperty'
---
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
