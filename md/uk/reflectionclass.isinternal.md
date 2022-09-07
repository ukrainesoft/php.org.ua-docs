---
navigation:
  - reflectionclass.isinterface.md: '« ReflectionClass::isInterface'
  - reflectionclass.isiterable.md: 'ReflectionClass::isIterable »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isInternal'
---
# ReflectionClass::isInternal

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isInternal — Перевіряє, чи клас вбудований у модуль або в ядро

### Опис

```methodsynopsis
public ReflectionClass::isInternal(): bool
```

Перевіряє, чи клас вбудований в модуль або в ядро, а не користувальницьким.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::isInternal()****

```php
<?php
$internalclass = new ReflectionClass('ReflectionClass');

class Apple {}
$userclass = new ReflectionClass('Apple');

var_dump($internalclass->isInternal());
var_dump($userclass->isInternal());
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionClass::isUserDefined()](reflectionclass.isuserdefined.md) - Перевіряє, чи є клас для користувача
