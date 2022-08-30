Перевіряє, чи визначено властивість у конструкторі

-   [« ReflectionProperty::isPrivate](reflectionproperty.isprivate.html)
    
-   [ReflectionProperty::isProtected »](reflectionproperty.isprotected.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionProperty](class.reflectionproperty.html)
    
-   Перевіряє, чи визначено властивість у конструкторі
    

# ReflectionProperty::isPromoted

(PHP 8)

ReflectionProperty::isPromoted — Перевіряє, чи визначено властивість у конструкторі

### Опис

```methodsynopsis
public ReflectionProperty::isPromoted(): bool
```

Перевіряє, [чи визначено властивість у конструкторі](language.oop5.decon.html#language.oop5.decon.constructor.promotion)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо властивість визначено в конструкторі, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::isPromoted()****

```php
<?php
class Foo {
    public $baz;

    public function __construct(public $bar) {}
}

$o = new Foo(42);
$o->baz = 42;

$ro = new ReflectionObject($o);
var_dump($ro->getProperty('bar')->isPromoted());
var_dump($ro->getProperty('baz')->isPromoted());
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionProperty::isDefault()](reflectionproperty.isdefault.html) - Перевіряє, чи є значення властивістю за умовчанням
-   [ReflectionProperty::isInitialized()](reflectionproperty.isinitialized.html) - Перевірити, чи ініціалізована властивість
-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.html) - набуває значення