Отримати тип властивості

-   [« ReflectionProperty::getName](reflectionproperty.getname.html)
    
-   [ReflectionProperty::getValue »](reflectionproperty.getvalue.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionProperty](class.reflectionproperty.html)
    
-   Отримати тип властивості
    

# ReflectionProperty::getType

(PHP 7> = 7.4.0, PHP 8)

ReflectionProperty::getType — Отримати тип властивості

### Опис

```methodsynopsis
public ReflectionProperty::getType(): ?ReflectionType
```

Повертає тип якості.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [ReflectionType](class.reflectiontype.html)якщо для властивості заданий тип, або **`null`** якщо ні.

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::getType()****

```php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
echo $rp->getType()->getName();
?>
```

Результат виконання цього прикладу:

```
string
```

### Дивіться також

-   [ReflectionProperty::hasType()](reflectionproperty.hastype.html) - Перевірити, чи заданий для властивості тип
-   [ReflectionProperty::isInitialized()](reflectionproperty.isinitialized.html) - Перевірити, чи ініціалізована властивість