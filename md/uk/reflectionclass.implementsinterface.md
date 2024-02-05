---
navigation:
  - reflectionclass.hasproperty.md: '« ReflectionClass::hasProperty'
  - reflectionclass.innamespace.md: 'ReflectionClass::inNamespace »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::implementsInterface'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::implementsInterface

(PHP 5, PHP 7, PHP 8)

ReflectionClass::implementsInterface — Перевіряє, чи реалізується інтерфейс

### Опис

```methodsynopsis
public ReflectionClass::implementsInterface(ReflectionClass|string $interface): bool
```

Перевіряє, чи реалізує клас зазначений інтерфейс чи ні.

### Список параметрів

`interface`

Ім'я інтерфейсу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**ReflectionClass::implementsInterface()** викидає [ReflectionException](class.reflectionexception.md), якщо `interface` не є інтерфейсом.

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) \- Перевіряє, чи є клас інтерфейсом
-   [ReflectionClass::isSubclassOf()](reflectionclass.issubclassof.md) \- Перевіряє, чи є клас підкласом
-   [interface\_exists()](function.interface-exists.md) \- Перевіряє, чи визначено інтерфейс
-   [Інтерфейси об'єктів](language.oop5.interfaces.md)
