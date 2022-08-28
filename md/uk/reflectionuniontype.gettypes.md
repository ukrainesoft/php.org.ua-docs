Повертає типи, включені до типу union

-   [« ReflectionUnionType](class.reflectionuniontype.html)
    
-   [ReflectionGenerator »](class.reflectiongenerator.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionUnionType](class.reflectionuniontype.html)
    
-   Повертає типи, включені до типу union
    

# ReflectionUnionType::getTypes

(PHP 8)

ReflectionUnionType::getTypes — Повертає типи, включені до типу union

### Опис

```methodsynopsis
public ReflectionUnionType::getTypes(): array
```

Повертає відображення типів, включених у тип union.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів [ReflectionType](class.reflectiontype.html)

### Приклади

**Приклад #1 Приклад використання **ReflectionUnionType::getTypes()****

```php
<?php
function someFunction(int|float $number) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

var_dump($reflectionParam->getType()->getTypes());
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

-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.html) - Перевіряє, чи допустимо NULL
-   [ReflectionParameter::getType()](reflectionparameter.gettype.html) - Отримати тип параметра