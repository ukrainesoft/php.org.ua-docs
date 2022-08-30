Визначає, чи є у функції попередній тип значення, що повертається

-   [« ReflectionFunctionAbstract::hasReturnType](reflectionfunctionabstract.hasreturntype.html)
    
-   [ReflectionFunctionAbstract::inNamespace »](reflectionfunctionabstract.innamespace.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunctionAbstract](class.reflectionfunctionabstract.html)
    
-   Визначає, чи є у функції попередній тип значення, що повертається
    

# ReflectionFunctionAbstract::hasTentativeReturnType

(PHP 8> = 8.1.0)

ReflectionFunctionAbstract::hasTentativeReturnType — Визначає, чи є у функції попередній тип значення, що повертається

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::hasTentativeReturnType(): bool
```

Визначає, чи є у функції попередній тип значення, що повертається.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо у функції є попередній тип значення, що повертається, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionFunctionAbstract::hasTentativeReturnType()****

```php
<?php

$method = new ReflectionMethod(\ArrayAccess::class, 'offsetGet');
var_dump($method->hasTentativeReturnType());
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionFunctionAbstract::getTentativeReturnType()](reflectionfunctionabstract.gettentativereturntype.html) - Повертає попередній тип значення, що повертається, пов'язаний з функцією
-   [ReflectionFunctionAbstract::hasReturnType()](reflectionfunctionabstract.hasreturntype.html) - Перевіряє, чи має функція оголошений тип значення, що повертається
-   [Сумісність типів значень, що повертаються, з внутрішніми класами](language.oop5.inheritance.html#language.oop5.inheritance.internal-classes)