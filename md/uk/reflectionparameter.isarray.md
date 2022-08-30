Перевіряє, чи очікує аргумент масив як значення

-   [« ReflectionParameter::hasType](reflectionparameter.hastype.md)
    
-   [ReflectionParameter::isCallable »](reflectionparameter.iscallable.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionParameter](class.reflectionparameter.md)
    
-   Перевіряє, чи очікує аргумент масив як значення
    

# ReflectionParameter::isArray

(PHP 5> = 5.1.2, PHP 7, PHP 8)

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

**`true`**, якщо як значення очікується масив (array), **`false`** в іншому випадку.

### Приклади

**Приклад #1 Альтернатива у PHP 8.0.0**

Починаючи з PHP 8.0.0, наступний код повідомить, чи підтримує тип об'єкти, що викликаються, в тому числі як частина об'єднання.

```php
<?php
function declaresArray(ReflectionParameter $reflectionParameter): bool
{
    $reflectionType = $reflectionParameter->getType();

    if (!$reflectionType) return false;

    $types = $reflectionType instanceof ReflectionUnionType
        ? $reflectionType->getTypes()
        : [$reflectionType];

   return in_array('array', array_map(fn(ReflectionNamedType $t) => $t->getName(), $types));
}
?>
```

### Дивіться також

-   [ReflectionParameter::isOptional()](reflectionparameter.isoptional.md) - Перевіряє, чи є аргумент необов'язковим