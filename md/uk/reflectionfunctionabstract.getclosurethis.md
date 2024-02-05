---
navigation:
  - reflectionfunctionabstract.getclosurescopeclass.md: '« ReflectionFunctionAbstract::getClosureScopeClass'
  - reflectionfunctionabstract.getclosureusedvariables.md: 'ReflectionFunctionAbstract::getClosureUsedVariables »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getClosureThis'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getClosureThis

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::getClosureThis — Повертає вказівник, прив'язаний до замикання

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getClosureThis(): ?object
```

Отримує об'єкт, пов'язаний з $this всередині замикання, якщо функція є нестатичним замиканням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає покажчик $this. Повертає \*\*`null`\*\*в случае возникновения ошибки.
