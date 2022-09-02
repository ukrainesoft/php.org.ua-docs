---
navigation:
  - mongodb-driver-cursor.current.md: '« MongoDBDriverCursor::current'
  - mongodb-driver-cursor.getserver.md: 'MongoDBDriverCursor::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDBDriverCursor
title: 'MongoDBDriverCursor::getId'
---
# MongoDBDriverCursor::getId

(mongodb >=1.0.0)

MongoDBDriverCursor::getId — Повертає ідентифікатор для курсору

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md), пов'язаний із цим курсором. Ідентифікатор курсору однозначно ідентифікує курсор на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md) для курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverCursor::getId()****

```php
<?php

/* В этом примере мы добавляем несколько документов в коллекцию и указываем
 * меньший batchSize, чтобы гарантировать, что первая порция содержит только
 * подмножество наших результатов и курсор остаётся открытым на сервере. */
$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump($cursor->getId());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MongoDB\Driver\CursorId)#5 (1) {
  ["id"]=>
  int(94810124093)
}
```

### Дивіться також

-   [MongoDBDriverCursorId](class.mongodb-driver-cursorid.md)
-   [MongoDBDriverCursorId::toString()](mongodb-driver-cursorid.tostring.md) - Строкове подання ідентифікатора курсору
