---
navigation:
  - componere-abstract-definition.addinterface.md: '« ComponereAbstractDefinition::addInterface'
  - componere-abstract-definition.addtrait.md: 'ComponereAbstractDefinition::addTrait »'
  - index.md: PHP Manual
  - class.componere-abstract-definition.md: ComponereAbstractDefinition
title: 'ComponereAbstractDefinition::addMethod'
---
# ComponereAbstractDefinition::addMethod

(Componere 2 >= 2.1.0)

ComponereAbstractDefinition::addMethod — Додає метод

### Опис

```methodsynopsis
public Componere\Abstract\Definition::addMethod(string $name, Componere\Method $method): Definition
```

Повинен створити чи перевизначити метод у поточному визначенні.

### Список параметрів

`name`

Нечутливе до регістру ім'я методу

`method`

[ComponereMethod](class.componere-method.md) раніше не доданий до іншого Definition

### Значення, що повертаються

The current Definition

### Exceptions

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо метод був доданий до іншого визначення
