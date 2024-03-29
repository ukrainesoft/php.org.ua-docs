---
navigation:
  - reflectionextension.istemporary.md: '« ReflectionExtension::isTemporary'
  - class.reflectionfunction.md: ReflectionFunction »
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::\_\_function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::\_\_toString — Перетворення на рядок

### Опис

```methodsynopsis
public ReflectionExtension::__toString(): string
```

Виконує експорт модуля та повертає його у вигляді рядка string. Це те саме, що й виклик [ReflectionExtension::export()](reflectionextension.export.md) з аргументом `return`, рівним **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає експортований модуль у вигляді рядка, так само як [ReflectionExtension::export()](reflectionextension.export.md)

### Дивіться також

-   [ReflectionExtension::\_\_construct()](reflectionextension.construct.md) \- Створює об'єкт класу ReflectionExtension
-   [ReflectionExtension::export()](reflectionextension.export.md) \- Експортує модуль
-   [\_\_toString()](language.oop5.magic.md#object.tostring)
