Перевіряє, чи є функція застарілої

-   [« ReflectionFunctionAbstract::isClosure](reflectionfunctionabstract.isclosure.html)
    
-   [ReflectionFunctionAbstract::isGenerator »](reflectionfunctionabstract.isgenerator.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFunctionAbstract](class.reflectionfunctionabstract.html)
    
-   Перевіряє, чи є функція застарілої
    

# ReflectionFunctionAbstract::isDeprecated

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::isDeprecated — Перевіряє, чи функція застаріла

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::isDeprecated(): bool
```

Перевіряє, чи функція застаріла.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо функція застаріла, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ReflectionFunctionAbstract::isDeprecated()****

```php
<?php
$rf = new ReflectionFunction('ereg');
var_dump($rf->isDeprecated());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionFunctionAbstract::getDocComment()](reflectionfunctionabstract.getdoccomment.html) - Отримує doc-коментар