---
navigation:
  - class.reflectiontype.md: « ReflectionType
  - reflectiontype.tostring.md: 'ReflectionType::\_\_toString »'
  - index.md: PHP Manual
  - class.reflectiontype.md: ReflectionType
title: 'ReflectionType::allowsNull'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionType::allowsNull

(PHP 7, PHP 8)

ReflectionType::allowsNull — Перевіряє, чи допустимо NULL

### Опис

```methodsynopsis
public ReflectionType::allowsNull(): bool
```

Перевіряє, чи припустимо \*\*`null`\*\*в заданном параметре.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо **`null`**допустим, иначе**`false`**

### Приклади

**Пример #1 Пример использования**ReflectionType::allowsNull()\*\*\*\*

```php
<?php
function someFunction(string $param, stdClass $param2 = null) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->getType()->allowsNull());
var_dump($reflectionParams[1]->getType()->allowsNull());
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionNamedType::isBuiltin()](reflectionnamedtype.isbuiltin.md) \- Перевіряє, чи є тип вбудованим
-   [ReflectionType::\_\_toString()](reflectiontype.tostring.md) \- Перетворення на рядок
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) \- Отримати тип параметра
