Перевіряє, чи має функція оголошений тип значення, що повертається

-   [« ReflectionFunctionAbstract::getTentativeReturnType](reflectionfunctionabstract.gettentativereturntype.html)
    
-   [ReflectionFunctionAbstract::hasTentativeReturnType »](reflectionfunctionabstract.hastentativereturntype.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunctionAbstract](class.reflectionfunctionabstract.html)
    
-   Перевіряє, чи має функція оголошений тип значення, що повертається
    

# ReflectionFunctionAbstract::hasReturnType

(PHP 7, PHP 8)

ReflectionFunctionAbstract::hasReturnType — Перевіряє, чи має функція оголошений тип значення, що повертається

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::hasReturnType(): bool
```

Перевіряє, чи має функція оголошений тип значення, що повертається.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо функція має оголошений тип значення, що повертається, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад **ReflectionFunctionAbstract::hasReturnType()****

```php
<?php

function to_int($param) : int {
    return (int) $param;
}

$reflection1 = new ReflectionFunction('to_int');
var_dump($reflection1->hasReturnType());
```

Результат виконання цього прикладу:

```
bool(true)
```

**Приклад #2 Застосування до вбудованих функцій**

```php
<?php

$reflection2 = new ReflectionFunction('array_merge');

var_dump($reflection2->hasReturnType());
```

Результат виконання цього прикладу:

```
bool(false)
```

Це відбувається через те, що багато внутрішніх функцій не мають оголошених типів для аргументів або значення, що повертається. Тому краще уникати використання цього методу на внутрішніх функціях.

### Дивіться також

-   [ReflectionFunctionAbstract::getReturnType()](reflectionfunctionabstract.getreturntype.html) - Отримує оголошений тип значення, що повертається функцією значення