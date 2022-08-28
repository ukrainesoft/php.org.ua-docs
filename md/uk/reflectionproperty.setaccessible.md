Робить властивість доступною

-   [« ReflectionProperty::isStatic](reflectionproperty.isstatic.html)
    
-   [ReflectionProperty::setValue »](reflectionproperty.setvalue.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionProperty](class.reflectionproperty.html)
    
-   Робить властивість доступною
    

# ReflectionProperty::setAccessible

(PHP 5> = 5.3.0, PHP 7, PHP 8)

ReflectionProperty::setAccessible — Робить властивість доступним

### Опис

```methodsynopsis
public ReflectionProperty::setAccessible(bool $accessible): void
```

Забезпечує доступ до захищеної або закритої властивості за допомогою методів [ReflectionProperty::getValue()](reflectionproperty.getvalue.html) і [ReflectionProperty::setValue()](reflectionproperty.setvalue.html)

> **Зауваження**: Починаючи з PHP 8.1.0, виклик методу не має сенсу; всі методи викликаються за умовчанням.

### Список параметрів

`accessible`

**`true`** робить властивість доступною, **`false`** - Закриває доступ до властивості.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Визначення простого класу**

```php
<?php
class MyClass
{
    private $foo = 'bar';
}

$property = new ReflectionProperty("MyClass", "foo");
$property->setAccessible(true);

$obj = new MyClass();
echo $property->getValue($obj);
echo $obj->foo;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bar
Fatal error: Uncaught Error: Cannot access private property MyClass::$foo in /in/WJqTv:12
```

### Дивіться також

-   [ReflectionProperty::isPrivate()](reflectionproperty.isprivate.html) - Перевіряє, чи властивість закрита
-   [ReflectionProperty::isProtected()](reflectionproperty.isprotected.html) - Перевіряє, чи властивість захищена