---
navigation:
  - reflectionparameter.hastype.md: '« ReflectionParameter::hasType'
  - reflectionparameter.iscallable.md: 'ReflectionParameter::isCallable »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::isArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::isArray

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

ReflectionParameter::isArray — Перевіряє, чи очікує аргумент масив як значення

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

У наведеному нижче прикладі показаний альтернативний спосіб отримання цієї інформації.

### Опис

```methodsynopsis
public ReflectionParameter::isArray(): bool
```

Перевіряє, чи очікує аргумент масив як значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо в якості значення очікується масив (array), **`false`** в іншому випадку.

### Приклади

**Приклад #1 Альтернатива у PHP 8.0.0**

Починаючи з PHP 8.0.0, наступний код повідомить, чи підтримує тип об'єкти, що викликаються, в тому числі як частина об'єднання.

```php
<?php
function declaresArray(ReflectionParameter $reflectionParameter): bool
{
    $reflectionType = $reflectionParameter->getType();

    if (!$reflectionType) return false;

    $types = $reflectionType instanceof ReflectionUnionType
        ? $reflectionType->getTypes()
        : [$reflectionType];

   return in_array('array', array_map(fn(ReflectionNamedType $t) => $t->getName(), $types));
}
?>
```

### Дивіться також

-   [ReflectionParameter::isOptional()](reflectionparameter.isoptional.md) \- Перевіряє, чи є аргумент необов'язковим
