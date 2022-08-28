Отримує оголошений тип значення, що повертається функцією значення

-   [« ReflectionFunctionAbstract::getParameters](reflectionfunctionabstract.getparameters.html)
    
-   [ReflectionFunctionAbstract::getShortName »](reflectionfunctionabstract.getshortname.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunctionAbstract](class.reflectionfunctionabstract.html)
    
-   Отримує оголошений тип значення, що повертається функцією значення
    

# ReflectionFunctionAbstract::getReturnType

(PHP 7, PHP 8)

ReflectionFunctionAbstract::getReturnType — Отримує оголошений тип значення, що повертається функцією значення

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getReturnType(): ?ReflectionType
```

Отримує оголошений тип значення, що повертається функцією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт класу [ReflectionType](class.reflectiontype.html), якщо у функції оголошено тип значення, що повертається, **`null`** в іншому випадку.

### Приклади

**Приклад #1 Приклад **ReflectionFunctionAbstract::getReturnType()****

```php
<?php

function to_int($param) : int {
    return (int) $param;
}

$reflection1 = new ReflectionFunction('to_int');
echo $reflection1->getReturnType();
```

Результат виконання цього прикладу:

```
int
```

**Приклад #2 Застосування до вбудованих функцій**

```php
<?php

$reflection2 = new ReflectionFunction('array_merge');

var_dump($reflection2->getReturnType());
```

Результат виконання цього прикладу:

```
null
```

Це відбувається через те, що багато внутрішніх функцій не мають оголошених типів для аргументів або значення, що повертається. Тому краще уникати використання цього методу на вбудованих функціях.

### Дивіться також

-   [ReflectionFunctionAbstract::hasReturnType()](reflectionfunctionabstract.hasreturntype.html) - Перевіряє, чи має функція оголошений тип значення, що повертається
-   [ReflectionType::\_\_toString()](reflectiontype.tostring.html) - Перетворення на рядок