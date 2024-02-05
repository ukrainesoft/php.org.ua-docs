---
navigation:
  - reflectionclass.newinstanceargs.md: '« ReflectionClass::newInstanceArgs'
  - reflectionclass.setstaticpropertyvalue.md: 'ReflectionClass::setStaticPropertyValue »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::newInstanceWithoutConstructor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::newInstanceWithoutConstructor

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionClass::newInstanceWithoutConstructor — Створює новий екземпляр класу без виклику конструктора

### Опис

```methodsynopsis
public ReflectionClass::newInstanceWithoutConstructor(): object
```

Створює новий екземпляр класу без виклику конструктора.

### Список параметрів

### Значення, що повертаються

### Помилки

Якщо клас є вбудованим, і його екземпляр не може бути створений без виклику конструктора, це призведе до генерації виключення [ReflectionException](class.reflectionexception.md). Цей виняток обмежений лише класами з модифікатором [final](language.oop5.final.md)

### Дивіться також

-   [ReflectionClass::newInstance()](reflectionclass.newinstance.md) \- створює екземпляр класу з переданими аргументами
-   [ReflectionClass::newInstanceArgs()](reflectionclass.newinstanceargs.md) \- Створює екземпляр класу з переданими параметрами
