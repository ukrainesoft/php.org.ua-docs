Повертає будь-які помилки запису, що відбулися

-   [« MongoDB\\Driver\\WriteResult::getWriteConcernError](mongodb-driver-writeresult.getwriteconcernerror.html)
    
-   [MongoDB\\Driver\\WriteResult::isAcknowledged »](mongodb-driver-writeresult.isacknowledged.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html)
    
-   Повертає будь-які помилки запису, що відбулися
    

# MongoDBDriverWriteResult::getWriteErrors

(mongodb >=1.0.0)

MongoDBDriverWriteResult::getWriteErrors — Повертає будь-які помилки запису, що відбулися

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteResult::getWriteErrors(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html) для будь-яких помилок запису, виявлених під час операції запису. Масив буде порожнім, якщо помилок не сталося.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteResult::getWriteErrors()** з однією помилкою**

```php
<?php

$manager = new MongoDB\Driver\Manager;

/* По умолчанию массовые операции записи выполняются последовательно по порядку
 * и выполнение прекращается после первой ошибки.
 */
$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 3]);
$bulk->insert(['_id' => 4]);
$bulk->insert(['_id' => 4]);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  object(MongoDB\Driver\WriteError)#5 (4) {
    ["message"]=>
    string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 2 }"
    ["code"]=>
    int(11000)
    ["index"]=>
    int(2)
    ["info"]=>
    NULL
  }
}
```

**Приклад #2 Приклад використання **MongoDBDriverWriteResult::getWriteErrors()** з кількома помилками**

```php
<?php

$manager = new MongoDB\Driver\Manager;

/* Параметр "ordered" может использоваться для продолжения
 * выполнения массовых операций записи после первой ошибки.
 */
$bulk = new MongoDB\Driver\BulkWrite(['ordered' => false]);
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 3]);
$bulk->insert(['_id' => 4]);
$bulk->insert(['_id' => 4]);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors());
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  [0]=>
  object(MongoDB\Driver\WriteError)#5 (4) {
    ["message"]=>
    string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 2 }"
    ["code"]=>
    int(11000)
    ["index"]=>
    int(2)
    ["info"]=>
    NULL
  }
  [1]=>
  object(MongoDB\Driver\WriteError)#6 (4) {
    ["message"]=>
    string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 4 }"
    ["code"]=>
    int(11000)
    ["index"]=>
    int(5)
    ["info"]=>
    NULL
  }
}
```

### Дивіться також

-   [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html)