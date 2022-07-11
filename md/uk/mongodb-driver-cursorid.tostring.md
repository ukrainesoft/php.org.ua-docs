- [« MongoDB\Driver\CursorId::serialize](mongodb-driver-cursorid.serialize.md)
- [MongoDB\Driver\CursorId::unserialize »](mongodb-driver-cursorid.unserialize.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\CursorId](class.mongodb-driver-cursorid.md)
- Строкове представлення ідентифікатора курсору

# MongoDB\Driver\CursorId::\_\_toString

(mongodb \>=1.0.0)

MongoDB\Driver\CursorId::\_\_toString - Строкове уявлення
ідентифікатора курсору

### Опис

final public **MongoDB\Driver\CursorId::\_\_toString**(): string

Повертає ідентифікатор курсору як рядка (string).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор курсору як рядка (string).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\CursorId::\_\_toString()****

`<?php/* В цьому прикладі ми додаємо документи в колекцію і вказуємо * менший batchSize, щоб гарантувати, що перша порція над на те  */$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['x' => 1]);$bulk->insert(['x' => 2]);$bulk->insert(['x' => 3]);$manager->executeBulkWrite('db.collection', $bulk);$cursor = $manager->executeQuery('db.collection', $query);var_dump((string) $cursor->getId( ));?> `

Результатом виконання цього прикладу буде щось подібне:

string(11) "98061641158"

### Дивіться також

- [MongoDB\Driver\Cursor::getId()](mongodb-driver-cursor.getid.md) -
Повертає ідентифікатор для курсору
