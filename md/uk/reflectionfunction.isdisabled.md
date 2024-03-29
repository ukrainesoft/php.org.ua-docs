---
navigation:
  - reflectionfunction.isanonymous.md: '« ReflectionFunction::isAnonymous'
  - reflectionfunction.tostring.md: 'ReflectionFunction::\_\_toString »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::isDisabled'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunction::isDisabled

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ReflectionFunction::isDisabled — Перевіряє, що функція вимкнена

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
public ReflectionFunction::isDisabled(): bool
```

Перевіряє, чи функція вимкнена, за допомогою директиви [disable\_functions](ini.core.md#ini.disable-functions)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо функцію вимкнено, **`false`** інакше.

### Дивіться також

-   [ReflectionFunctionAbstract::isUserDefined()](reflectionfunctionabstract.isuserdefined.md) \- Перевіряє, чи функція є певною користувачем
-   [Директива disable\_functions](ini.core.md#ini.disable-functions)
