---
navigation:
  - reflectionfunction.invokeargs.md: '« ReflectionFunction::invokeArgs'
  - reflectionfunction.isdisabled.md: 'ReflectionFunction::isDisabled »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::isAnonymous'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunction::isAnonymous

(PHP 8 >= 8.2.0)

ReflectionFunction::isAnonymous — Перевіряє, чи є функція анонімною

### Опис

```methodsynopsis
public ReflectionFunction::isAnonymous(): bool
```

Перевіряє, чи є функція [анонімний](functions.anonymous.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо функція анонімна, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** ReflectionFunction::isAnonymous()\*\*\*\*

```php
<?php

$rf = new ReflectionFunction(function() {});
var_dump($rf->isAnonymous());

$rf = new ReflectionFunction('strlen');
var_dump($rf->isAnonymous());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [Анонімні функції](functions.anonymous.md)
