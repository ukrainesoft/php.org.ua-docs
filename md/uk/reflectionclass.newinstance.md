---
navigation:
  - reflectionclass.isuserdefined.md: '« ReflectionClass::isUserDefined'
  - reflectionclass.newinstanceargs.md: 'ReflectionClass::newInstanceArgs »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::newInstance'
---
# ReflectionClass::newInstance

(PHP 5, PHP 7, PHP 8)

ReflectionClass::newInstance — Створює екземпляр класу з переданими аргументами

### Опис

```methodsynopsis
public ReflectionClass::newInstance(mixed ...$args): object
```

Створює новий екземпляр класу. Прийняті аргументи передаються конструктор класу.

### Список параметрів

`args`

Приймає довільну кількість аргументів, подібно до функції [calluserfunc()](function.call-user-func.md), які потім передаються конструктор класу.

### Значення, що повертаються

### Помилки

Якщо конструктор не є загальнодоступним (public), це призведе до викидання винятку [ReflectionException](class.reflectionexception.md)

Якщо конструктор відсутня, а параметр `args` має один і більше аргументів, то це призведе до викидання винятку [ReflectionException](class.reflectionexception.md)

### Дивіться також

-   [ReflectionClass::newInstanceArgs()](reflectionclass.newinstanceargs.md) - Створює екземпляр класу з переданими параметрами
-   [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.md) - Створює новий екземпляр класу без виклику конструктора
