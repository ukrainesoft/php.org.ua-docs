---
navigation:
  - reflectionnamedtype.getname.html: '« ReflectionNamedType::getName'
  - class.reflectionobject.html: ReflectionObject »
  - index.html: PHP Manual
  - class.reflectionnamedtype.html: ReflectionNamedType
title: 'ReflectionNamedType::isBuiltin'
---
# ReflectionNamedType::isBuiltin

(PHP 7, PHP 8)

ReflectionNamedType::isBuiltin — Перевіряє, чи є тип вбудованим

### Опис

```methodsynopsis
public ReflectionNamedType::isBuiltin(): bool
```

Перевіряє, чи тип вбудованого типу PHP. Вбудований тип - будь-який тип, який не є класом, інтерфейсом або трейтом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо тип вбудований, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ReflectionNamedType::isBuiltin()****

```php
<?php
class SomeClass {}

function someFunction(string $param, SomeClass $param2, StdClass $param3) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->getType()->isBuiltin());
var_dump($reflectionParams[1]->getType()->isBuiltin());
var_dump($reflectionParams[2]->getType()->isBuiltin());
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(false)
```

Зауважте, що метод **ReflectionNamedType::isBuiltin()** не розрізняє внутрішні та користувальницькі класи. Щоб їх розрізнити, потрібно використати метод [ReflectionClass::isInternal()](reflectionclass.isinternal.html) для імені класу, що повертається.

### Дивіться також

-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.html) - Перевіряє, чи допустимо NULL
-   [ReflectionType::toString()](reflectiontype.tostring.html) - Перетворення на рядок
-   [ReflectionClass::isInternal()](reflectionclass.isinternal.html) - Перевіряє, чи є клас вбудованим у модуль чи ядро
-   [ReflectionParameter::getType()](reflectionparameter.gettype.html) - Отримати тип параметра
