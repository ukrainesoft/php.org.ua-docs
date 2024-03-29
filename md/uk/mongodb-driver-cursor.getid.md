---
navigation:
  - mongodb-driver-cursor.current.md: '« MongoDB\\Driver\\Cursor::current'
  - mongodb-driver-cursor.getserver.md: 'MongoDB\\Driver\\Cursor::getServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDB\\Driver\\Cursor
title: 'MongoDB\\Driver\\Cursor::getId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Cursor::getId

(mongodb >=1.0.0)

MongoDB\\Driver\\Cursor::getId — Повертає ідентифікатор для курсору

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md), пов'язаний із цим курсором. Ідентифікатор курсору однозначно ідентифікує курсор на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md)для курсора.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Cursor::getId()\*\*\*\*

```php
<?php

/* В этом Прикладе мы добавляем несколько документов в коллекцию и указываем
 * меньший batchSize, чтобы гарантировать, что первая порция содержит только
 * подмножество наших результатов и курсор остаётся открытым на сервере. */
$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump($cursor->getId());

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\Driver\CursorId)#5 (1) {
  ["id"]=>
  int(94810124093)
}
```

### Дивіться також

-   [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md)
-   [MongoDB\\Driver\\CursorId::\_\_toString()](mongodb-driver-cursorid.tostring.md) \- Строкове подання ідентифікатора курсору
