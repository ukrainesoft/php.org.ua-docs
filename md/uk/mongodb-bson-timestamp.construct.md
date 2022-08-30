Створює новий Timestamp

-   [« MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)
    
-   [MongoDBBSONTimestamp::getIncrement »](mongodb-bson-timestamp.getincrement.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)
    
-   Створює новий Timestamp
    

# MongoDBBSONTimestamp::construct

(mongodb >=1.0.0)

MongoDBBSONTimestamp::construct - Створює новий Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::__construct(int $increment, int $timestamp)
```

### Список параметрів

`increment` (int)

32-розрядне ціле число, що означає порядковий номер, що збільшується, для операцій протягом цієї секунди.

`timestamp` (int)

32-розрядне ціле число, що означає секунди з початку епохи Unix.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONTimestamp::construct()****

```php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\BSON\Timestamp)#1 (2) {
  ["increment"]=>
  int(1234)
  ["timestamp"]=>
  int(5678)
}
```

### Дивіться також

-   [» Типы BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)