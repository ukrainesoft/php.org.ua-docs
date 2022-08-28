Перевірити, чи заданий для властивості тип

-   [« ReflectionProperty::hasDefaultValue](reflectionproperty.hasdefaultvalue.html)
    
-   [ReflectionProperty::isDefault »](reflectionproperty.isdefault.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionProperty](class.reflectionproperty.html)
    
-   Перевірити, чи заданий для властивості тип
    

# ReflectionProperty::hasType

(PHP 7> = 7.4.0, PHP 8)

ReflectionProperty::hasType — Перевірити, чи заданий для властивості тип

### Опис

```methodsynopsis
public ReflectionProperty::hasType(): bool
```

Перевірити, чи заданий для властивості тип.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо тип заданий, то **`true`**, а якщо ні, то **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::hasType()****

```php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
var_dump($rp->hasType());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionProperty::getType()](reflectionproperty.gettype.html) - Отримати тип властивості
-   [ReflectionProperty::isInitialized()](reflectionproperty.isinitialized.html) - Перевірити, чи ініціалізована властивість