---
navigation:
  - reflectionproperty.getdeclaringclass.md: '« ReflectionProperty::getDeclaringClass'
  - reflectionproperty.getdoccomment.md: 'ReflectionProperty::getDocComment »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::getDefaultValue'
---
# ReflectionProperty::getDefaultValue

(PHP 8)

ReflectionProperty::getDefaultValue — Повертає значення за промовчанням, задане для властивості

### Опис

```methodsynopsis
public ReflectionProperty::getDefaultValue(): mixed
```

Повертає явно чи неявно задане значення за умовчанням властивості.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення за замовчуванням (включаючи **`null`**), якщо воно задано. Якщо значення за замовчуванням не задано, то повертається **`null`**. Для визначення того, чи встановлено в принципі значення за промовчанням для властивості, використовуйте [ReflectionProperty::hasDefaultValue()](reflectionproperty.hasdefaultvalue.md)

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::getDefaultValue()****

```php
<?php
class Foo {
    public $bar = 1;
    public ?int $baz;
    public int $boing = 0;
}

$ro = new ReflectionClass(Foo::class);
var_dump($ro->getProperty('bar')->getDefaultValue());
var_dump($ro->getProperty('baz')->getDefaultValue());
var_dump($ro->getProperty('boing')->getDefaultValue());
?>
```

Результат виконання цього прикладу:

```
int(1)
NULL
int(0)
```

### Дивіться також

-   [ReflectionProperty::hasDefaultValue()](reflectionproperty.hasdefaultvalue.md) - Перевіряє, чи встановлено значення за промовчанням.
