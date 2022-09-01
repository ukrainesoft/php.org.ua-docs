---
navigation:
  - reflectionfunction.invokeargs.md: '« ReflectionFunction::invokeArgs'
  - reflectionfunction.tostring.md: 'ReflectionFunction::toString »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::isDisabled'
---
# ReflectionFunction::isDisabled

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ReflectionFunction::isDisabled — Перевіряє, що функція вимкнена

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
public ReflectionFunction::isDisabled(): bool
```

Перевіряє, чи функція вимкнена, за допомогою директиви [disablefunctions](ini.core.html#ini.disable-functions)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо функцію вимкнено, **`false`** інакше.

### Дивіться також

-   [ReflectionFunctionAbstract::isUserDefined()](reflectionfunctionabstract.isuserdefined.md) - Перевіряє, чи функція є певною користувачем
-   [Директива disablefunctions](ini.core.html#ini.disable-functions)
