---
navigation:
  - reflectionfunctionabstract.innamespace.md: '« ReflectionFunctionAbstract::inNamespace'
  - reflectionfunctionabstract.isdeprecated.md: 'ReflectionFunctionAbstract::isDeprecated »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::isClosure'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::isClosure

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

ReflectionFunctionAbstract::isClosure — Перевіряє, чи є функція замиканням ([Closure](class.closure.md)) .

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::isClosure(): bool
```

Перевірка, чи є функція замикання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо функція є замиканням ([Closure](class.closure.md) **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования метода**ReflectionFunctionAbstract::isClosure()\*\*\*\*

```php
<?php
// Не замыкание
$function1 = 'str_replace';
$reflection1 = new ReflectionFunction($function1);
var_dump($reflection1->isClosure());

// Замыкание
$function2 = function () {};
$reflection2 = new ReflectionFunction($function2);
var_dump($reflection2->isClosure());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionFunctionAbstract::isGenerator()](reflectionfunctionabstract.isgenerator.md) \- Перевіряє, чи є функція генератором
