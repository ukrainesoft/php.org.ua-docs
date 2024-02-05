---
navigation:
  - reflectionclass.isreadonly.md: '« ReflectionClass::isReadOnly'
  - reflectionclass.istrait.md: 'ReflectionClass::isTrait »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isSubclassOf'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isSubclassOf

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isSubclassOf — Перевіряє, чи клас підкласом

### Опис

```methodsynopsis
public ReflectionClass::isSubclassOf(ReflectionClass|string $class): bool
```

Перевіряє, чи клас підкласом зазначеного класу чи реалізує зазначений інтерфейс.

### Список параметрів

`class`

Рядок з ім'ям класу, що перевіряється, або об'єкт класу [ReflectionClass](class.reflectionclass.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) \- Перевіряє, чи є клас інтерфейсом
-   [ReflectionClass::implementsInterface()](reflectionclass.implementsinterface.md) \- Перевіряє, чи реалізується інтерфейс
-   [is\_subclass\_of()](function.is-subclass-of.md) \- Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
-   [get\_parent\_class()](function.get-parent-class.md) \- Повертає ім'я батьківського класу для об'єкта чи класу
