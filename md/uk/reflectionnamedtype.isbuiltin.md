---
navigation:
  - reflectionnamedtype.getname.md: '« ReflectionNamedType::getName'
  - class.reflectionobject.md: ReflectionObject »
  - index.md: PHP Manual
  - class.reflectionnamedtype.md: ReflectionNamedType
title: 'ReflectionNamedType::isBuiltin'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Приклад #1 Приклад використання** ReflectionNamedType::isBuiltin()\*\*\*\*

```php
<?php
class SomeClass {}

function someFunction(string $param, SomeClass $param2, stdClass $param3) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->getType()->isBuiltin());
var_dump($reflectionParams[1]->getType()->isBuiltin());
var_dump($reflectionParams[2]->getType()->isBuiltin());
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
```

Заметьте, что метод**ReflectionNamedType::isBuiltin()** не розрізняє внутрішні та користувальницькі класи. Щоб їх розрізнити, потрібно використати метод [ReflectionClass::isInternal()](reflectionclass.isinternal.md)для возвращаемого имени класса.

### Дивіться також

-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.md) \- Перевіряє, чи допустимо NULL
-   [ReflectionType::\_\_toString()](reflectiontype.tostring.md) \- Перетворення на рядок
-   [ReflectionClass::isInternal()](reflectionclass.isinternal.md) \- Перевіряє, чи клас вбудований в модуль або в ядро
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) \- Отримати тип параметра
