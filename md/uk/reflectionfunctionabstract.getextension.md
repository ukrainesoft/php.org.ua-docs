---
navigation:
  - reflectionfunctionabstract.getendline.md: '« ReflectionFunctionAbstract::getEndLine'
  - reflectionfunctionabstract.getextensionname.md: 'ReflectionFunctionAbstract::getExtensionName »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getExtension'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getExtension

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::getExtension — Отримує інформацію про модуль

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getExtension(): ?ReflectionExtension
```

Отримання інформації про модуль, до складу якого входить функція.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Інформація про модуль як об'єкт [ReflectionExtension](class.reflectionextension.md)или\*\*`null`\*\* для функцій користувача.

### Дивіться також

-   [ReflectionFunctionAbstract::getExtensionName()](reflectionfunctionabstract.getextensionname.md) \- Отримання імені модуля
