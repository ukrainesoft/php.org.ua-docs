---
navigation:
  - reflectionclass.getattributes.md: '« ReflectionClass::getAttributes'
  - reflectionclass.getconstants.md: 'ReflectionClass::getConstants »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getConstant'
---
# ReflectionClass::getConstant

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getConstant — Повертає певну константу

### Опис

```methodsynopsis
public ReflectionClass::getConstant(string $name): mixed
```

Повертає певну константу.

### Список параметрів

`name`

Назва константи класу.

### Значення, що повертаються

Значення константи з ім'ям `name`. Повертає **`false`** якщо константа відсутня у класі.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getConstant()****

```php
<?php

class Example {
    const C1 = false;
    const C2 = 'I am a constant';
}

$reflection = new ReflectionClass('Example');

var_dump($reflection->getConstant('C1'));
var_dump($reflection->getConstant('C2'));
var_dump($reflection->getConstant('C3'));
?>
```

Результат виконання цього прикладу:

```
bool(false)
string(15) "I am a constant"
bool(false)
```

### Дивіться також

-   [ReflectionClass::getConstants()](reflectionclass.getconstants.md) - Повертає константи
