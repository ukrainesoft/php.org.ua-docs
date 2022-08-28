Повертає ідентифікатор для курсору

-   [« MongoDB\\Driver\\Cursor::current](mongodb-driver-cursor.current.html)
    
-   [MongoDB\\Driver\\Cursor::getServer »](mongodb-driver-cursor.getserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
    
-   Повертає ідентифікатор для курсору
    

# MongoDBDriverCursor::getId

(mongodb >=1.0.0)

MongoDBDriverCursor::getId — Повертає ідентифікатор для курсору

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html), пов'язаний із цим курсором. Ідентифікатор курсору однозначно ідентифікує курсор на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html) для курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

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

-   [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html)
-   [MongoDB\\Driver\\CursorId::\_\_toString()](mongodb-driver-cursorid.tostring.html) - Строкове подання ідентифікатора курсору