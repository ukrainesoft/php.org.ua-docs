---
navigation:
  - reflectionparameter.isarray.md: '« ReflectionParameter::isArray'
  - reflectionparameter.isdefaultvalueavailable.md: 'ReflectionParameter::isDefaultValueAvailable »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::isCallable'
---
# ReflectionParameter::isCallable

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionParameter::isCallable — Визначити, чи параметр має бути типу callable

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

У наведеному нижче прикладі показаний альтернативний спосіб отримання цієї інформації.

### Опис

```methodsynopsis
public ReflectionParameter::isCallable(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо параметр [callable](language.types.callable.md) **`false`** в іншому випадку. У разі виникнення помилки поверне **`null`**

### Приклади

**Приклад #1 Альтернатива у PHP 8.0.0**

Починаючи з PHP 8.0.0, наступний код повідомить, чи підтримує тип об'єкти, що викликаються, в тому числі як частина об'єднання.

```php
<?php
function declaresCallable(ReflectionParameter $reflectionParameter): bool
{
    $reflectionType = $reflectionParameter->getType();

    if (!$reflectionType) return false;

    $types = $reflectionType instanceof ReflectionUnionType
        ? $reflectionType->getTypes()
        : [$reflectionType];

   return in_array('callable', array_map(fn(ReflectionNamedType $t) => $t->getName(), $types));
}
?>
```
