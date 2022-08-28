Повертає кількість документів, вибраних для оновлення

-   [« MongoDB\\Driver\\WriteResult::getInsertedCount](mongodb-driver-writeresult.getinsertedcount.html)
    
-   [MongoDB\\Driver\\WriteResult::getModifiedCount »](mongodb-driver-writeresult.getmodifiedcount.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає кількість документів, вибраних для оновлення
    

# MongoDBDriverWriteResult::getMatchedCount

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getMatchedCount — Повертає кількість документів, вибраних для оновлення

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getMatchedCount(): ?int
```

Якщо операція оновлення не призводить до зміни документа (наприклад, встановлення значення поля в його поточне значення), зіставлена ​​кількість може бути більшою, ніж значення, що повертається [MongoDB\\Driver\\WriteResult::getModifiedCount()](mongodb-driver-writeresult.getmodifiedcount.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість документів, вибраних для оновлення, або **`null`** якщо запис не було підтверджено.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getMatchedCount()****

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getMatchedCount());

?>
```

Результат виконання цього прикладу:

```
int(1)
```

### Дивіться також

-   [MongoDB\\Driver\\WriteResult::getModifiedCount()](mongodb-driver-writeresult.getmodifiedcount.html) - Повертає кількість існуючих оновлених документів
-   [MongoDB\\Driver\\WriteResult::isAcknowledged()](mongodb-driver-writeresult.isacknowledged.html) - Повертає, чи був запис підтверджений