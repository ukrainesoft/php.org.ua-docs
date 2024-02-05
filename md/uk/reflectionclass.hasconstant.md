---
navigation:
  - reflectionclass.gettraits.md: '« ReflectionClass::getTraits'
  - reflectionclass.hasmethod.md: 'ReflectionClass::hasMethod »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::hasConstant'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::hasConstant

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання** ReflectionClass::hasConstant()\*\*\*\*

```php
<?php
class Foo {
    const c1 = 1;
}

$class = new ReflectionClass("Foo");

var_dump($class->hasConstant("c1"));
var_dump($class->hasConstant("c2"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionClass::hasMethod()](reflectionclass.hasmethod.md) \- Перевіряє, чи заданий метод
-   [ReflectionClass::hasProperty()](reflectionclass.hasproperty.md) \- Перевіряє, чи визначено властивість
