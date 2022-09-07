---
navigation:
  - reflectionproperty.getvalue.md: '« ReflectionProperty::getValue'
  - reflectionproperty.hastype.md: 'ReflectionProperty::hasType »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::hasDefaultValue'
---
# ReflectionProperty::hasDefaultValue

(PHP 8)

ReflectionProperty::hasDefaultValue — Перевіряє, чи встановлено значення за промовчанням.

### Опис

```methodsynopsis
public ReflectionProperty::hasDefaultValue(): bool
```

Перевіряє, чи встановлено значення за промовчанням для властивості, включаючи **`null`**. Повертає **`false`** для типизованих властивостей без заданого значення за умовчанням і динамічних властивостей.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо для властивості встановлено значення за замовчуванням (включаючи **`null`**), то повертає **`true`**. Якщо властивість типізована і для нього не задано значення за умовчанням, або якщо це властиво, що динамічно визначається, то повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::hasDefaultValue()****

```php
<?php
class Foo {
    public $bar;
    public ?int $baz;
    public ?int $foo = null;
    public int $boing;

    public function __construct()
    {
        $this->ping = '';
    }
}

$ro = new ReflectionObject(new Foo());
var_dump($ro->getProperty('bar')->hasDefaultValue());
var_dump($ro->getProperty('baz')->hasDefaultValue());
var_dump($ro->getProperty('foo')->hasDefaultValue());
var_dump($ro->getProperty('boing')->hasDefaultValue());
var_dump($ro->getProperty('ping')->hasDefaultValue()); // Динамическое свойство
var_dump($ro->getProperty('pong')->hasDefaultValue()); // Неопределённое свойство
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(true)
bool(false)
bool(false)

Fatal error: Uncaught ReflectionException: Property Foo::$pong does not exist in example.php
```

### Дивіться також

-   [ReflectionProperty::getDefaultValue()](reflectionproperty.getdefaultvalue.md) - Повертає значення за промовчанням, задане для якості
