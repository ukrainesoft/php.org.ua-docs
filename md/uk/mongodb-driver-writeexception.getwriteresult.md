---
navigation:
  - class.mongodb-driver-exception-writeexception.md: « MongoDB\\Driver\\Exception\\WriteException
  - mongodb.exceptions.tree.md: Class Tree »
  - index.md: PHP Manual
  - class.mongodb-driver-exception-writeexception.md: MongoDB\\Driver\\Exception\\WriteException
title: 'MongoDB\\Driver\\Exception\\WriteException::getWriteResult'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Exception\\WriteException::getWriteResult

(mongodb >= 1.0.0)

MongoDB\\Driver\\Exception\\WriteException::getWriteResult — Повертає WriteResult для операції запису помилкою, що закінчилася.

### Опис

```methodsynopsis
final public MongoDB\Driver\Exception\WriteException::getWriteResult(): MongoDB\Driver\WriteResult
```

Повертає об'єкт [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md) для операції запису, що закінчилася помилкою. Більш детальну інформацію про помилку можна отримати за допомогою методів [MongoDB\\Driver\\WriteResult::getWriteErrors()](mongodb-driver-writeresult.getwriteerrors.md) і [MongoDB\\Driver\\WriteResult::getWriteConcernError()](mongodb-driver-writeresult.getwriteconcernerror.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md) для операції запису помилкою, що закінчилася.

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\Exception\\WriteException::getWriteResult()\*\*\*\*

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost');
$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\WriteException $e) {
    $writeResult = $e->getWriteResult();

    if ($writeConcernError = $writeResult->getWriteConcernError()) {
        var_dump($writeConcernError);
    }

    if ($writeErrors = $writeResult->getWriteErrors()) {
        var_dump($writeErrors);
    }
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [0]=>
  object(MongoDB\Driver\WriteError)#5 (4) {
    ["message"]=>
    string(70) "E11000 duplicate key error index: db.collection.$_id_ dup key: { : 1 }"
    ["code"]=>
    int(11000)
    ["index"]=>
    int(1)
    ["info"]=>
    NULL
  }
}
```

### Дивіться також

-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) \- Виконує одну або кілька операцій запису
