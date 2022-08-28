Повертає екземпляр ReflectionProperty для якості класу

-   [« ReflectionClass::getProperties](reflectionclass.getproperties.html)
    
-   [ReflectionClass::getReflectionConstant »](reflectionclass.getreflectionconstant.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає екземпляр ReflectionProperty для якості класу
    

# ReflectionClass::getProperty

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getProperty — Повертає екземпляр [ReflectionProperty](class.reflectionproperty.html) для якості класу

### Опис

```methodsynopsis
public ReflectionClass::getProperty(string $name): ReflectionProperty
```

Повертає екземпляр [ReflectionProperty](class.reflectionproperty.html) для якості класу.

### Список параметрів

`name`

Ім'я якості.

### Значення, що повертаються

Об'єкт класу [ReflectionProperty](class.reflectionproperty.html)

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getProperty()****

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$property = $class->getProperty('name');
var_dump($property);
?>
```

Результат виконання цього прикладу:

```
object(ReflectionProperty)#2 (2) {
  ["name"]=>
  string(4) "name"
  ["class"]=>
  string(15) "ReflectionClass"
}
```

### Дивіться також

-   [ReflectionClass::getProperties()](reflectionclass.getproperties.html) - Повертає властивості