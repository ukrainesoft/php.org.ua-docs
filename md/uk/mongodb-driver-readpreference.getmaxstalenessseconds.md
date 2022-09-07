---
navigation:
  - mongodb-driver-readpreference.gethedge.md: '« MongoDBDriverReadPreference::getHedge'
  - mongodb-driver-readpreference.getmode.md: 'MongoDBDriverReadPreference::getMode »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDBDriverReadPreference
title: 'MongoDBDriverReadPreference::getMaxStalenessSeconds'
---
# MongoDBDriverReadPreference::getMaxStalenessSeconds

(mongodb >=1.2.0)

MongoDBDriverReadPreference::getMaxStalenessSeconds — Повертає параметр "maxStalenessSeconds" ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getMaxStalenessSeconds(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає параметр "maxStalenessSeconds" ReadPreference. Якщо не вказано максимальну staleness, повертається **`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadPreference::getMaxStalenessSeconds()****

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => MongoDB\Driver\ReadPreference::NO_MAX_STALENESS,
]);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS,
]);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => 1000,
]);
var_dump($rp->getMaxStalenessSeconds());

?>
```

Результат виконання цього прикладу:

```
int(-1)
int(-1)
int(90)
int(1000)
```

### Дивіться також

-   [» Руководство по предпочтению чтения](https://www.mongodb.com/docs/manual/core/read-preference/)
