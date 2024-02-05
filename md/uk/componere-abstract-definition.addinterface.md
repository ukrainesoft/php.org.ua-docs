---
navigation:
  - class.componere-abstract-definition.md: « Componere\\Abstract\\Definition
  - componere-abstract-definition.addmethod.md: 'Componere\\Abstract\\Definition::addMethod »'
  - index.md: PHP Manual
  - class.componere-abstract-definition.md: Componere\\Abstract\\Definition
title: 'Componere\\Abstract\\Definition::addInterface'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Abstract\\Definition::addInterface

(Componere 2 >= 2.1.0)

Componere\\Abstract\\Definition::addInterface — Додає інтерфейс

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
