---
navigation:
  - reflectionproperty.hastype.md: '« ReflectionProperty::hasType'
  - reflectionproperty.isinitialized.md: 'ReflectionProperty::isInitialized »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::isDefault'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::isDefault

(PHP 5, PHP 7, PHP 8)

ReflectionProperty::isDefault — Перевіряє, чи є значення властивістю за промовчанням

### Опис

```methodsynopsis
public ReflectionProperty::isDefault(): bool
```

Перевіряє, чи є значення властивістю, заданою на етапі компіляції, або встановлено динамічно під час виконання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо властивість оголошено під час компіляції, або **`false`**, якщо його було створено під час виконання.

### Приклади

**Пример #1 Пример использования**ReflectionProperty::isDefault()\*\*\*\*

```php
<?php
class Foo {
    public $bar;
}

$o = new Foo();
$o->bar = 42;
$o->baz = 42;

$ro = new ReflectionObject($o);
var_dump($ro->getProperty('bar')->isDefault());
var_dump($ro->getProperty('baz')->isDefault());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.md) \- набуває значення
