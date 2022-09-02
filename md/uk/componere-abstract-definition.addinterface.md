---
navigation:
  - class.componere-abstract-definition.md: « ComponereAbstractDefinition
  - componere-abstract-definition.addmethod.md: 'ComponereAbstractDefinition::addMethod »'
  - index.md: PHP Manual
  - class.componere-abstract-definition.md: ComponereAbstractDefinition
title: 'ComponereAbstractDefinition::addInterface'
---
# ComponereAbstractDefinition::addInterface

(Componere 2 >= 2.1.0)

ComponereAbstractDefinition::addInterface — Додає інтерфейс

### Опис

```methodsynopsis
public Componere\Abstract\Definition::addInterface(string $interface): Definition
```

Реалізує цей інтерфейс за поточним визначенням

### Список параметрів

`interface`

Ім'я інтерфейсу без урахування регістру

### Значення, що повертаються

The current Definition

### Exceptions

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition було зареєстровано
