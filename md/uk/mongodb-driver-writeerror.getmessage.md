---
navigation:
  - mongodb-driver-writeerror.getinfo.md: '« MongoDB\\Driver\\WriteError::getInfo'
  - class.mongodb-driver-writeresult.md: MongoDB\\Driver\\WriteResult »
  - index.md: PHP Manual
  - class.mongodb-driver-writeerror.md: MongoDB\\Driver\\WriteError
title: 'MongoDB\\Driver\\WriteError::getMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteError::getMessage

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteError::getMessage — Повертає повідомлення про помилку WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getMessage(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку WriteError.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteError::getMessage()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getMessage());
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(70) "E11000 duplicate key error index: db.collection.$_id_ dup key: { : 1 }"
```
