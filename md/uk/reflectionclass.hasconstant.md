---
navigation:
  - reflectionclass.gettraits.html: '« ReflectionClass::getTraits'
  - reflectionclass.hasmethod.html: 'ReflectionClass::hasMethod »'
  - index.html: PHP Manual
  - class.reflectionclass.html: ReflectionClass
title: 'ReflectionClass::hasConstant'
---
# ReflectionClass::hasConstant

(PHP 5> = 5.1.2, PHP 7, PHP 8)

ReflectionClass::hasConstant — Перевіряє, чи визначена константа

### Опис

```methodsynopsis
public ReflectionClass::hasConstant(string $name): bool
```

Перевіряє, чи в класі визначена зазначена константа чи ні.

### Список параметрів

`name`

Ім'я константи, що перевіряється.

### Значення, що повертаються

\*\*`true`\*\*якщо константа визначена, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::hasConstant()****

```php
<?php
class Foo {
    const c1 = 1;
}

$class = new ReflectionClass("Foo");

var_dump($class->hasConstant("c1"));
var_dump($class->hasConstant("c2"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionClass::hasMethod()](reflectionclass.hasmethod.html) - Перевіряє, чи заданий метод
-   [ReflectionClass::hasProperty()](reflectionclass.hasproperty.html) - Перевіряє, чи визначено властивість
