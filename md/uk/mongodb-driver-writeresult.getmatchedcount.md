- [« MongoDB\Driver\WriteResult::getInsertedCount](mongodb-driver-writeresult.getinsertedcount.md)
- [MongoDB\Driver\WriteResult::getModifiedCount »](mongodb-driver-writeresult.getmodifiedcount.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\WriteResult](class.mongodb-driver-writeresult.md)
- Повертає кількість документів, вибраних для оновлення

# MongoDB\Driver\WriteResult::getMatchedCount

(mongodb \>=1.0.0)

MongoDB\Driver\WriteResult::getMatchedCount — Повертає кількість
документів, вибраних для оновлення

### Опис

final public **MongoDB\Driver\WriteResult::getMatchedCount**(): ?int

Якщо операція оновлення не змінює документ (наприклад,
встановлення значення поля в його поточне значення), зіставлене
кількість може бути більшою, ніж значення, що повертається
[MongoDB\Driver\WriteResult::getModifiedCount()](mongodb-driver-writeresult.getmodifiedcount.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість документів, вибраних для оновлення, або
**`null`** якщо запис не був підтверджений.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\WriteResult::getMatchedCount()****

` <?php$manager = new MongoDB\Driver\Manager;$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['x' => 1]);$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);$bulk->update(['x' => 2], ['$set' => ['y' = > 1]], ['upsert' => true]);$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert ' => true]);$bulk->delete(['x' => 1]);$result = $manager->executeBulkWrite('db.collection', $bulk);var_dump($result->getMatchedCount( ));?> `

Результат виконання цього прикладу:

int(1)

### Дивіться також

- [MongoDB\Driver\WriteResult::getModifiedCount()](mongodb-driver-writeresult.getmodifiedcount.md) -
Повертає кількість існуючих оновлених документів
- [MongoDB\Driver\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.md) -
Повертає, чи був запис підтверджений
