---
navigation:
  - componere-definition.construct.md: '« ComponereDefinition::construct'
  - componere-definition.addproperty.md: 'ComponereDefinition::addProperty »'
  - index.md: PHP Manual
  - class.componere-definition.md: ComponereDefinition
title: 'ComponereDefinition::addConstant'
---
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

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `name` вже оголошено як константа

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `value` є статичним

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `value` є невизначеним
