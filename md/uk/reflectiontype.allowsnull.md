---
navigation:
  - class.reflectiontype.md: « ReflectionType
  - reflectiontype.tostring.md: 'ReflectionType::toString »'
  - index.md: PHP Manual
  - class.reflectiontype.md: ReflectionType
title: 'ReflectionType::allowsNull'
---
# ReflectionType::allowsNull

(PHP 7, PHP 8)

ReflectionType::allowsNull — Перевіряє, чи допустимо NULL

### Опис

```methodsynopsis
public ReflectionType::allowsNull(): bool
```

Перевіряє, чи припустимо **`null`** у заданому параметрі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо **`null`** припустимо, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionType::allowsNull()****

```php
<?php
function someFunction(string $param, StdClass $param2 = null) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->getType()->allowsNull());
var_dump($reflectionParams[1]->getType()->allowsNull());
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionNamedType::isBuiltin()](reflectionnamedtype.isbuiltin.md) - Перевіряє, чи є тип вбудованим
-   [ReflectionType::toString()](reflectiontype.tostring.md) - Перетворення на рядок
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) - Отримати тип параметра
