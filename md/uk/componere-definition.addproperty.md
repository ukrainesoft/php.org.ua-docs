---
navigation:
  - componere-definition.addconstant.md: '« Componere\\Definition::addConstant'
  - componere-definition.register.md: 'Componere\\Definition::register »'
  - index.md: PHP Manual
  - class.componere-definition.md: Componere\\Definition
title: 'Componere\\Definition::addProperty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Definition::addProperty

(Componere 2 >= 2.1.0)

Componere\\Definition::addProperty — Додає властивість

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

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `name` вже оголошено як властивість
