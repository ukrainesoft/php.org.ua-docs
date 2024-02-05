---
navigation:
  - mongodb-driver-cursorid.serialize.md: '« MongoDB\\Driver\\CursorId::serialize'
  - mongodb-driver-cursorid.unserialize.md: 'MongoDB\\Driver\\CursorId::unserialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorid.md: MongoDB\\Driver\\CursorId
title: 'MongoDB\\Driver\\CursorId::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorId::\_\_function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDB\\Driver\\CursorId::\_\_toString — Строкове представлення ідентифікатора курсору

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::__toString(): string
```

Повертає ідентифікатор курсору у вигляді рядка (string).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор курсору у вигляді рядка (string).

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\CursorId::\_\_toString()\*\*\*\*

```php
<?php

/* В этом примере мы добавляем документы в коллекцию и указываем
 * меньший batchSize, чтобы гарантировать, что первая порция содержит только подмножество
 * наших результатов и курсор остаётся открытым на сервере. */
$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump((string) $cursor->getId());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "98061641158"
```

### Дивіться також

-   [MongoDB\\Driver\\Cursor::getId()](mongodb-driver-cursor.getid.md) \- Повертає ідентифікатор для курсору
