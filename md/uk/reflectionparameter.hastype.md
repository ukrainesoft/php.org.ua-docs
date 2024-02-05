---
navigation:
  - reflectionparameter.gettype.md: '« ReflectionParameter::getType'
  - reflectionparameter.isarray.md: 'ReflectionParameter::isArray »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::hasType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

**Приклад #1 Приклад використання** ReflectionParameter::hasType()\*\*\*\*

```php
<?php
function someFunction(string $param, $param2 = null) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->hasType());
var_dump($reflectionParams[1]->hasType());
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```

### Дивіться також

-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) \- Отримати тип параметра
