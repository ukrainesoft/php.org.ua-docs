Повертає строкову виставу Timestamp

-   [« MongoDBBSONTimestamp::serialize](mongodb-bson-timestamp.serialize.html)
    
-   [MongoDBBSONTimestamp::unserialize »](mongodb-bson-timestamp.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html)
    
-   Повертає строкову виставу Timestamp
    

# MongoDBBSONTimestamp::function toString() { \[native code\] }

(mongodb >=1.0.0)

MongoDBBSONTimestamp::toString — Повертає строкову виставу Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Timestamp.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONTimestamp::toString()****

```php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);
var_dump((string) $timestamp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "[1234:5678]"
```

### Дивіться також

-   [» Типы BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)