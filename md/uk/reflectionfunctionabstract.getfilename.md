---
navigation:
  - reflectionfunctionabstract.getextensionname.md: '« ReflectionFunctionAbstract::getExtensionName'
  - reflectionfunctionabstract.getname.md: 'ReflectionFunctionAbstract::getName »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getFileName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getFileName

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::getFileName — Отримує ім'я файлу

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getFileName(): string|false
```

Отримує ім'я файлу з певною функцією користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, в якому було визначено функцію. Повертає **`false`**, якщо клас визначений у ядрі PHP або модулі PHP.

### Дивіться також

-   [ReflectionFunctionAbstract::getNamespaceName()](reflectionfunctionabstract.getnamespacename.md) \- Отримання імені простору імен
