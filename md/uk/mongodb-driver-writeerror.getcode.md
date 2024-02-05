---
navigation:
  - class.mongodb-driver-writeerror.md: « MongoDB\\Driver\\WriteError
  - mongodb-driver-writeerror.getindex.md: 'MongoDB\\Driver\\WriteError::getIndex »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeerror.md: MongoDB\\Driver\\WriteError
title: 'MongoDB\\Driver\\WriteError::getCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteError::getCode

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteError::getCode — Повертає код помилки WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getCode(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код помилки WriteError.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteError::getCode()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getCode());
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(11000)
```
