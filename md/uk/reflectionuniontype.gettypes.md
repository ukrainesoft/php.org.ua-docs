---
navigation:
  - class.reflectionuniontype.md: « ReflectionUnionType
  - class.reflectiongenerator.md: ReflectionGenerator »
  - index.md: PHP Manual
  - class.reflectionuniontype.md: ReflectionUnionType
title: 'ReflectionUnionType::getTypes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionUnionType::getTypes

(PHP 8)

ReflectionUnionType::getTypes — Повертає типи, включені до типу union

### Опис

```methodsynopsis
public ReflectionUnionType::getTypes(): array
```

Повертає відображення типів, включених у тип union.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів [ReflectionType](class.reflectiontype.md)

### Приклади

**Пример #1 Пример использования**ReflectionUnionType::getTypes()\*\*\*\*

```php
<?php
function someFunction(int|float $number) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

var_dump($reflectionParam->getType()->getTypes());
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
