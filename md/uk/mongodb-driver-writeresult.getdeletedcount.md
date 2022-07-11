- [« MongoDB\Driver\WriteResult](class.mongodb-driver-writeresult.md)
- [MongoDB\Driver\WriteResult::getInsertedCount »](mongodb-driver-writeresult.getinsertedcount.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\WriteResult](class.mongodb-driver-writeresult.md)
- Повертає кількість видалених документів

# MongoDB\Driver\WriteResult::getDeletedCount

(mongodb \>=1.0.0)

MongoDB\Driver\WriteResult::getDeletedCount — Повертає кількість
віддалених документів

### Опис

final public **MongoDB\Driver\WriteResult::getDeletedCount**(): ?int

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість видалених документів або **`null`** якщо запис не
була підтверджена.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\WriteResult::getDeletedCount()****

` <?php$manager = new MongoDB\Driver\Manager;$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['x' => 1]);$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);$bulk->update(['x' => 2], ['$set' => ['y' = > 1]], ['upsert' => true]);$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert ' => true]);$bulk->delete(['x' => 1]);$result = $manager->executeBulkWrite('db.collection', $bulk);var_dump($result->getDeletedCount( ));?> `

Результат виконання цього прикладу:

int(1)

### Дивіться також

- [MongoDB\Driver\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) -
Повертає, чи був запис підтверджений
