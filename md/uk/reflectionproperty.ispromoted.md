---
navigation:
  - reflectionproperty.isprivate.md: '« ReflectionProperty::isPrivate'
  - reflectionproperty.isprotected.md: 'ReflectionProperty::isProtected »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::isPromoted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::isPromoted

(PHP 8)

ReflectionProperty::isPromoted — Перевіряє, чи визначено властивість у конструкторі

### Опис

```methodsynopsis
public ReflectionProperty::isPromoted(): bool
```

Перевіряє, [чи визначено властивість у конструкторі](language.oop5.decon.md#language.oop5.decon.constructor.promotion)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо властивість визначена в конструкторі, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** ReflectionProperty::isPromoted()\*\*\*\*

```php
<?php
class Foo {
    public $baz;

    public function __construct(public $bar) {}
}

$o = new Foo(42);
$o->baz = 42;

$ro = new ReflectionObject($o);
var_dump($ro->getProperty('bar')->isPromoted());
var_dump($ro->getProperty('baz')->isPromoted());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionProperty::isDefault()](reflectionproperty.isdefault.md) \- Перевіряє, чи є значення властивістю за умовчанням
-   [ReflectionProperty::isInitialized()](reflectionproperty.isinitialized.md) \- Перевірити, чи ініціалізована властивість
-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.md) \- набуває значення
