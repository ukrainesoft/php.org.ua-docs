---
navigation:
  - reflectionclass.isiterateable.md: '« ReflectionClass::isIterateable'
  - reflectionclass.istrait.md: 'ReflectionClass::isTrait »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isSubclassOf'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) - Перевіряє, чи є клас інтерфейсом
-   [ReflectionClass::implementsInterface()](reflectionclass.implementsinterface.md) - Перевіряє, чи реалізується інтерфейс
-   [ісsubclassof()](function.is-subclass-of.md) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
-   [getparentclass()](function.get-parent-class.md) - Повертає ім'я батьківського класу для об'єкта чи класу
