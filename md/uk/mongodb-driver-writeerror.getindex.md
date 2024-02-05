---
navigation:
  - mongodb-driver-writeerror.getcode.md: '« MongoDB\\Driver\\WriteError::getCode'
  - mongodb-driver-writeerror.getinfo.md: 'MongoDB\\Driver\\WriteError::getInfo »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeerror.md: MongoDB\\Driver\\WriteError
title: 'MongoDB\\Driver\\WriteError::getIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteError::getIndex

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteError::getIndex — Повертає індекс запису, який відповідає цьому WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getIndex(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індекс запису (з [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)), що відповідає поточному WriteError.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\WriteError::getIndex()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getIndex());
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```

### Дивіться також

-   [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)
