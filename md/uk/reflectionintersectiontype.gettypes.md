Повертає типи, включені до типу intersection

-   [« ReflectionIntersectionType](class.reflectionintersectiontype.md)
    
-   [ReflectionReference »](class.reflectionreference.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionIntersectionType](class.reflectionintersectiontype.md)
    
-   Повертає типи, включені до типу intersection
    

# ReflectionIntersectionType::getTypes

(PHP 8> = 8.1.0)

ReflectionIntersectionType::getTypes — Повертає типи, включені до типу intersection

### Опис

```methodsynopsis
public ReflectionIntersectionType::getTypes(): array
```

Повертає типи, включені у тип intersection.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів [ReflectionType](class.reflectiontype.md)

### Приклади

**Приклад #1 Приклад використання **ReflectionIntersectionType::getTypes()****

```php
<?php

function someFunction(Iterator&Countable $value) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

var_dump($reflectionParam->getType()->getTypes());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
    [0] =>
    class ReflectionNamedType#4(0) {
    }
    [1] =>
    class ReflectionNamedType#5(0) {
    }
}
```

### Дивіться також

-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.md) - Перевіряє, чи допустимо NULL
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) - Отримати тип параметра