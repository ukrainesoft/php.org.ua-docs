---
navigation:
  - componere-definition.construct.md: '« Componere\\Definition::\_\_construct'
  - componere-definition.addproperty.md: 'Componere\\Definition::addProperty »'
  - index.md: PHP Manual
  - class.componere-definition.md: Componere\\Definition
title: 'Componere\\Definition::addConstant'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Definition::addConstant

(Componere 2 >= 2.1.0)

Componere\\Definition::addConstant — Додає константу

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

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `name` вже оголошено як константа

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `value` є статичним

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `value` є невизначеним
