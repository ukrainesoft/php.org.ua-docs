---
navigation:
  - reflectionclass.getextensionname.html: '« ReflectionClass::getExtensionName'
  - reflectionclass.getinterfacenames.html: 'ReflectionClass::getInterfaceNames »'
  - index.html: PHP Manual
  - class.reflectionclass.html: ReflectionClass
title: 'ReflectionClass::getFileName'
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

-   [ReflectionClass::getExtensionName()](reflectionclass.getextensionname.html) - Повертає ім'я модуля, що визначає клас
