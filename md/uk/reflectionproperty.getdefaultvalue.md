---
navigation:
  - reflectionproperty.getdeclaringclass.md: '« ReflectionProperty::getDeclaringClass'
  - reflectionproperty.getdoccomment.md: 'ReflectionProperty::getDocComment »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::getDefaultValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Значение по умолчанию (включая\*\*`null`**), если оно задано. Если значение по умолчанию не задано, то возвращается**`null`\*\*Для определения того, задано ли в принципе значение по умолчанию для свойства, используйте[ReflectionProperty::hasDefaultValue()](reflectionproperty.hasdefaultvalue.md)

### Приклади

**Приклад #1 Приклад використання** ReflectionProperty::getDefaultValue()\*\*\*\*

```php
<?php
class Foo {
    public $bar = 1;
    public ?int $baz;
    public int $boing = 0;
    public function __construct(public string $bak = "default") { }
}

$ro = new ReflectionClass(Foo::class);
var_dump($ro->getProperty('bar')->getDefaultValue());
var_dump($ro->getProperty('baz')->getDefaultValue());
var_dump($ro->getProperty('boing')->getDefaultValue());
var_dump($ro->getProperty('bak')->getDefaultValue());
?>
```

Результат виконання наведеного прикладу:

```
int(1)
NULL
int(0)
NULL
```

### Дивіться також

-   [ReflectionProperty::hasDefaultValue()](reflectionproperty.hasdefaultvalue.md) \- Перевіряє, чи встановлено значення за промовчанням.
