---
navigation:
  - reflectionfunctionabstract.getattributes.md: '« ReflectionFunctionAbstract::getAttributes'
  - reflectionfunctionabstract.getclosurethis.md: 'ReflectionFunctionAbstract::getClosureThis »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getClosureScopeClass'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getClosureScopeClass

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::getClosureScopeClass — Повертає клас, в рамках якого було оголошено замикання

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getClosureScopeClass(): ?ReflectionClass
```

Отримує клас, в рамках якого було оголошено замикання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає клас у разі успішного виконання або \*\*`null`\*\*якщо функція не є замиканням або якщо не було класу, в рамках якого оголошено замикання.
