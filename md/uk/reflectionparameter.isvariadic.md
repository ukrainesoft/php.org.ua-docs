---
navigation:
  - reflectionparameter.ispassedbyreference.md: '« ReflectionParameter::isPassedByReference'
  - reflectionparameter.tostring.md: 'ReflectionParameter::\_\_toString »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::isVariadic'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::isVariadic

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

ReflectionParameter::isVariadic — Перевірити, чи параметр є параметром зі змінною кількістю аргументів

### Опис

```methodsynopsis
public ReflectionParameter::isVariadic(): bool
```

Перевіряє, чи визначено параметр як [параметр зі змінною кількістю аргументів](functions.arguments.md#functions.variable-arg-list)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо параметр приймає змінну кількість аргументів, **`false`** в іншому випадку.
