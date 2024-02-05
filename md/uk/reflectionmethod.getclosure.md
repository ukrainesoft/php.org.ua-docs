---
navigation:
  - reflectionmethod.export.md: '« ReflectionMethod::export'
  - reflectionmethod.getdeclaringclass.md: 'ReflectionMethod::getDeclaringClass »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::getClosure'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::getClosure

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionMethod::getClosure — Повертає динамічно створене замикання для методу

### Опис

```methodsynopsis
public ReflectionMethod::getClosure(?object $object = null): Closure
```

Створює замикання, яке викликатиме метод.

### Список параметрів

`object`

Заборонений для статичних методів, є обов'язковим для інших.

### Значення, що повертаються

Повертає щойно створене замикання ([Closure](class.closure.md)

### Помилки

Викидає [ValueError](class.valueerror.md), якщо `object`является\*\*`null`\*\*Але метод є нестатичним.

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо `object` не є екземпляром класу, в якому було оголошено цей метод.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `object` тепер допускає значення null. |

### Дивіться також

-   [Callback-функції як об'єкти першого класу](functions.first_class_callable_syntax.md)
