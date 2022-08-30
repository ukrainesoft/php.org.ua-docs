Повертає, чи був запис підтверджений

-   [« MongoDBDriverWriteResult::getWriteErrors](mongodb-driver-writeresult.getwriteerrors.html)
    
-   [MongoDBBSON »](book.bson.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає, чи був запис підтверджений
    

# MongoDBDriverWriteResult::isAcknowledged

(mongodb >=1.0.0)

MongoDBDriverWriteResult::isAcknowledged — Повертає, чи був запис підтверджений

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::isAcknowledged(): bool
```

Якщо запис підтверджено, інші поля будуть доступні в об'єкті [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо запис було підтверджено, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::isAcknowledged()** з підтвердженими гарантіями запису**

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->isAcknowledged());

?>
```

Результат виконання цього прикладу:

```
bool(true)
```

**Приклад #2 Приклад використання **MongoDBDriverWriteResult::isAcknowledged()** з непідтвердженими гарантіями запису**

```php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk, new MongoDB\Driver\WriteConcern(0));

var_dump($result->isAcknowledged());

?>
```

Результат виконання цього прикладу:

```
bool(false)
```

### Дивіться також

-   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html)
-   [» Справка по гарантиям записи](https://www.mongodb.com/docs/manual/reference/write-concern/)