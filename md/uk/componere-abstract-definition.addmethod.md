---
navigation:
  - componere-abstract-definition.addinterface.md: '« Componere\\Abstract\\Definition::addInterface'
  - componere-abstract-definition.addtrait.md: 'Componere\\Abstract\\Definition::addTrait »'
  - index.md: PHP Manual
  - class.componere-abstract-definition.md: Componere\\Abstract\\Definition
title: 'Componere\\Abstract\\Definition::addMethod'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Abstract\\Definition::addMethod

(Componere 2 >= 2.1.0)

Componere\\Abstract\\Definition::addMethod — Додає метод

### Опис

```methodsynopsis
public Componere\Abstract\Definition::addMethod(string $name, Componere\Method $method): Definition
```

Повинен створити чи перевизначити метод у поточному визначенні.

### Список параметрів

`name`

Нечутливе до регістру ім'я методу

`method`

[Componere\\Method](class.componere-method.md) раніше не доданий до іншого Definition

### Значення, що повертаються

The current Definition

### Exceptions

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо метод був доданий до іншого визначення
