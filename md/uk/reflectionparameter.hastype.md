Перевірити, чи вказано тип параметра

-   [« ReflectionParameter::getType](reflectionparameter.gettype.md)
    
-   [ReflectionParameter::isArray »](reflectionparameter.isarray.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionParameter](class.reflectionparameter.md)
    
-   Перевірити, чи вказано тип параметра
    

# ReflectionParameter::hasType

(PHP 7, PHP 8)

ReflectionParameter::hasType — Перевірити, чи вказано тип параметра

### Опис

```methodsynopsis
public ReflectionParameter::hasType(): bool
```

Перевіряє, чи вказано тип параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо тип вказано, **`false`**, в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ReflectionParameter::hasType()****

```php
<?php
function someFunction(string $param, $param2 = null) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->hasType());
var_dump($reflectionParams[1]->hasType());
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) - Отримати тип параметра