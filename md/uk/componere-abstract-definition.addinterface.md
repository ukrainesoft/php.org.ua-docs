---
navigation:
  - class.componere-abstract-definition.html: « ComponereAbstractDefinition
  - componere-abstract-definition.addmethod.html: 'ComponereAbstractDefinition::addMethod »'
  - index.html: PHP Manual
  - class.componere-abstract-definition.html: ComponereAbstractDefinition
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

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо Definition було зареєстровано
