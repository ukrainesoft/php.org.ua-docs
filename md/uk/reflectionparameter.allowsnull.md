---
navigation:
  - class.reflectionparameter.md: « ReflectionParameter
  - reflectionparameter.canbepassedbyvalue.md: 'ReflectionParameter::canBePassedByValue »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::allowsNull'
---
# ReflectionParameter::allowsNull

(PHP 5, PHP 7, PHP 8)

ReflectionParameter::allowsNull — Перевіряє, чи допустимо значення null для параметра

### Опис

```methodsynopsis
public ReflectionParameter::allowsNull(): bool
```

Перевіряє, чи допустиме значення **`null`** для параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо **`null`** допускається, **`false`** в іншому випадку.

### Дивіться також

-   [ReflectionParameter::isOptional()](reflectionparameter.isoptional.md) - Перевіряє, чи є аргумент необов'язковим
