---
navigation:
  - class.reflectionintersectiontype.md: « ReflectionIntersectionType
  - class.reflectionreference.md: ReflectionReference »
  - index.md: PHP Manual
  - class.reflectionintersectiontype.md: ReflectionIntersectionType
title: 'ReflectionIntersectionType::getTypes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionIntersectionType::getTypes

(PHP 8 >= 8.1.0)

ReflectionIntersectionType::getTypes — Повертає типи, що перетинаються.

### Опис

```methodsynopsis
public ReflectionIntersectionType::getTypes(): array
```

Повертає типи, що перетинаються.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів [ReflectionType](class.reflectiontype.md)

### Приклади

**Пример #1 Пример использования метода**ReflectionIntersectionType::getTypes()\*\*\*\*

```php
<?php

function someFunction(Iterator&Countable $value) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

var_dump($reflectionParam->getType()->getTypes());
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.md) \- Перевіряє, чи допустимо NULL
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) \- Отримати тип параметра
