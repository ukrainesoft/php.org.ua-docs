- [« MongoDB\Driver\Cursor::current](mongodb-driver-cursor.current.md)
- [MongoDB\Driver\Cursor::getServer »](mongodb-driver-cursor.getserver.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)
- Повертає ідентифікатор для курсору

# MongoDB\Driver\Cursor::getId

(mongodb \>=1.0.0)

MongoDB\Driver\Cursor::getId — Повертає ідентифікатор для курсору

### Опис

final public **MongoDB\Driver\Cursor::getId**():
[MongoDB\Driver\CursorId](class.mongodb-driver-cursorid.md)

Повертає
[MongoDB\Driver\CursorId](class.mongodb-driver-cursorid.md), пов'язаний
із цим курсором. Ідентифікатор курсору однозначно ідентифікує курсор
на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\Driver\CursorId](class.mongodb-driver-cursorid.md)
для курсору.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання **MongoDB\Driver\Cursor::getId()****

`<?php/* У цьому прикладі ми додаємо кілька документів в колекцію і вказуємо * менший batchSize, щоб гарантувати, то| */$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['x' => 1]);$bulk->insert(['x' => 2]);$bulk->insert(['x' => 3]);$manager->executeBulkWrite('db.collection', $bulk);$cursor = $manager->executeQuery('db.collection', $query);var_dump($cursor->getId()); ?> `

Результатом виконання цього прикладу буде щось подібне:

object(MongoDB\Driver\CursorId)#5 (1) {
["id"]=>
int(94810124093)
}

### Дивіться також

- [MongoDB\Driver\CursorId](class.mongodb-driver-cursorid.md)
- [MongoDB\Driver\CursorId::\_\_toString()](mongodb-driver-cursorid.tostring.md) -
Строкове представлення ідентифікатора курсору
