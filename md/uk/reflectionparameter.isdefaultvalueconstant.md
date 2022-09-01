---
navigation:
  - reflectionparameter.isdefaultvalueavailable.html: '« ReflectionParameter::isDefaultValueAvailable'
  - reflectionparameter.isoptional.html: 'ReflectionParameter::isOptional »'
  - index.html: PHP Manual
  - class.reflectionparameter.html: ReflectionParameter
title: 'ReflectionParameter::isDefaultValueConstant'
---
# ReflectionParameter::isDefaultValueConstant

(PHP 5> = 5.4.6, PHP 7, PHP 8)

ReflectionParameter::isDefaultValueConstant — Визначити, чи є параметр за промовчанням константою

### Опис

```methodsynopsis
public ReflectionParameter::isDefaultValueConstant(): bool
```

Чи є константа значенням за промовчанням для цього параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо значення за промовчанням константа, **`false`**, в іншому випадку.

### Дивіться також

-   [ReflectionParameter::getDefaultValueConstantName()](reflectionparameter.getdefaultvalueconstantname.html) - Повертає ім'я константи значення за промовчанням, якщо значення за промовчанням константа або null
-   [ReflectionParameter::isDefaultValueAvailable()](reflectionparameter.isdefaultvalueavailable.html) - Перевіряє, чи є значення за замовчуванням
