---
navigation:
  - reflectionfunctionabstract.getnumberofrequiredparameters.md: '« ReflectionFunctionAbstract::getNumberOfRequiredParameters'
  - reflectionfunctionabstract.getreturntype.md: 'ReflectionFunctionAbstract::getReturnType »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getParameters'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getParameters

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::getParameters — Отримує параметри

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getParameters(): array
```

Отримання параметрів у вигляді масиву об'єктів [ReflectionParameter](class.reflectionparameter.md) у тому порядку, в якому вони визначені у джерелі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Параметри, представлені об'єктами [ReflectionParameter](class.reflectionparameter.md)

### Дивіться також

-   [ReflectionFunctionAbstract::getNumberOfParameters()](reflectionfunctionabstract.getnumberofparameters.md) \- Отримує кількість параметрів
-   [func\_get\_args()](function.func-get-args.md) \- Повертає масив, що містить аргументи функції
