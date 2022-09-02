---
navigation:
  - reflectionparameter.allowsnull.md: '« ReflectionParameter::allowsNull'
  - reflectionparameter.clone.md: 'ReflectionParameter::clone »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::canBePassedByValue'
---
# ReflectionParameter::canBePassedByValue

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionParameter::canBePassedByValue — Перевіряє, чи можна передати цей аргумент за значенням

### Опис

```methodsynopsis
public ReflectionParameter::canBePassedByValue(): bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо передача аргументу за значенням можлива, **`false`**, якщо ні. Повертає **`null`** у разі виникнення помилки.
