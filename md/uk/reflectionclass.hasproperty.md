---
navigation:
  - reflectionclass.hasmethod.md: '« ReflectionClass::hasMethod'
  - reflectionclass.implementsinterface.md: 'ReflectionClass::implementsInterface »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::hasProperty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::hasProperty

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

ReflectionClass::hasProperty — Перевіряє, чи визначено властивість

### Опис

```methodsynopsis
public ReflectionClass::hasProperty(string $name): bool
```

Перевіряє, чи в класі визначено зазначену властивість чи ні.

### Список параметрів

`name`

Ім'я властивості, що перевіряється.

### Значення, що повертаються

\*\*`true`\*\*якщо властивість задано, в іншому випадку **`false`**

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::hasProperty()\*\*\*\*

```php
<?php
class Foo {
    public    $p1;
    protected $p2;
    private   $p3;

}

$obj = new ReflectionObject(new Foo());

var_dump($obj->hasProperty("p1"));
var_dump($obj->hasProperty("p2"));
var_dump($obj->hasProperty("p3"));
var_dump($obj->hasProperty("p4"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionClass::hasConstant()](reflectionclass.hasconstant.md) \- Перевіряє, чи визначено константу
-   [ReflectionClass::hasMethod()](reflectionclass.hasmethod.md) \- Перевіряє, чи заданий метод
