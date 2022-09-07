---
navigation:
  - reflectionclass.getproperties.md: '« ReflectionClass::getProperties'
  - reflectionclass.getreflectionconstant.md: 'ReflectionClass::getReflectionConstant »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getProperty'
---
# ReflectionClass::getProperty

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getProperty — Повертає екземпляр [ReflectionProperty](class.reflectionproperty.md) для якості класу

### Опис

```methodsynopsis
public ReflectionClass::getProperty(string $name): ReflectionProperty
```

Повертає екземпляр [ReflectionProperty](class.reflectionproperty.md) для якості класу.

### Список параметрів

`name`

Ім'я якості.

### Значення, що повертаються

Об'єкт класу [ReflectionProperty](class.reflectionproperty.md)

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getProperty()****

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$property = $class->getProperty('name');
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

-   [ReflectionClass::getProperties()](reflectionclass.getproperties.md) - Повертає властивості
