---
navigation:
  - reflectionproperty.hastype.md: '« ReflectionProperty::hasType'
  - reflectionproperty.isinitialized.md: 'ReflectionProperty::isInitialized »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::isDefault'
---
# ReflectionProperty::isDefault

(PHP 5, PHP 7, PHP 8)

ReflectionProperty::isDefault — Перевіряє, чи значення є властивістю за умовчанням

### Опис

```methodsynopsis
public ReflectionProperty::isDefault(): bool
```

Перевіряє, чи є значення властивістю, заданою на етапі компіляції, або встановлено динамічно під час виконання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо властивість оголошено під час компіляції, або **`false`**, якщо він був створений під час виконання.

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::isDefault()****

```php
<?php
class Foo {
    public $bar;
}

$o = new Foo();
$o->bar = 42;
$o->baz = 42;

$ro = new ReflectionObject($o);
var_dump($ro->getProperty('bar')->isDefault());
var_dump($ro->getProperty('baz')->isDefault());
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.md) - набуває значення
