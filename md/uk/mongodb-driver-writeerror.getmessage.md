---
navigation:
  - mongodb-driver-writeerror.getinfo.html: '« MongoDBDriverWriteError::getInfo'
  - class.mongodb-driver-writeresult.html: MongoDBDriverWriteResult »
  - index.md: PHP Manual
  - class.mongodb-driver-writeerror.html: MongoDBDriverWriteError
title: 'MongoDBDriverWriteError::getMessage'
---
# MongoDBDriverWriteError::getMessage

(mongodb >=1.0.0)

MongoDBDriverWriteError::getMessage — Повертає повідомлення про помилку WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getMessage(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку WriteError.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteError::getMessage()****

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getMessage());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(70) "E11000 duplicate key error index: db.collection.$_id_ dup key: { : 1 }"
```
