---
navigation:
  - reflectionparameter.isdefaultvalueavailable.md: '« ReflectionParameter::isDefaultValueAvailable'
  - reflectionparameter.isoptional.md: 'ReflectionParameter::isOptional »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::isDefaultValueConstant'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::isDefaultValueConstant

(PHP 5 >= 5.4.6, PHP 7, PHP 8)

ReflectionParameter::isDefaultValueConstant — Визначити, чи є параметр за промовчанням константою

### Опис

```methodsynopsis
public ReflectionParameter::isDefaultValueConstant(): bool
```

Чи є константа значенням за промовчанням для цього параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если значение по умолчанию константа,**`false`**, в іншому випадку.

### Дивіться також

-   [ReflectionParameter::getDefaultValueConstantName()](reflectionparameter.getdefaultvalueconstantname.md) \- Повертає ім'я константи значення за промовчанням, якщо значення за промовчанням константа або null
-   [ReflectionParameter::isDefaultValueAvailable()](reflectionparameter.isdefaultvalueavailable.md) \- Перевіряє, чи є значення за замовчуванням
