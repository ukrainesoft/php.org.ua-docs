---
navigation:
  - componere-abstract-definition.addmethod.md: '« ComponereAbstractDefinition::addMethod'
  - componere-abstract-definition.getreflector.md: 'ComponereAbstractDefinition::getReflector »'
  - index.md: PHP Manual
  - class.componere-abstract-definition.md: ComponereAbstractDefinition
title: 'ComponereAbstractDefinition::addTrait'
---
# ComponereAbstractDefinition::addTrait

(Componere 2 >= 2.1.0)

ComponereAbstractDefinition::addTrait — Додає трейт

### Опис

```methodsynopsis
public Componere\Abstract\Definition::addTrait(string $trait): Definition
```

Використовувати цей трейт для поточного визначення

### Список параметрів

`trait`

Нечутливе до регістру ім'я трейту

### Значення, що повертаються

The current Definition

### Exceptions

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition було зареєстровано
