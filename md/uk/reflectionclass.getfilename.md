---
navigation:
  - reflectionclass.getextensionname.md: '« ReflectionClass::getExtensionName'
  - reflectionclass.getinterfacenames.md: 'ReflectionClass::getInterfaceNames »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getFileName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getFileName

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getFileName — Повертає ім'я файлу, в якому визначено клас

### Опис

```methodsynopsis
public ReflectionClass::getFileName(): string|false
```

Повертає ім'я файлу, у якому визначено клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, у якому визначено клас. Якщо клас визначено в ядрі PHP або модулі PHP, повертає **`false`**

### Дивіться також

-   [ReflectionClass::getExtensionName()](reflectionclass.getextensionname.md) \- Повертає ім'я модуля, що визначає клас
