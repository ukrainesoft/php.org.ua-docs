Повертає тип Binary

-   [« MongoDB\\BSON\\Binary::getData](mongodb-bson-binary.getdata.html)
    
-   [MongoDB\\BSON\\Binary::jsonSerialize »](mongodb-bson-binary.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)
    
-   Повертає тип Binary
    

# MongoDBBSONBinary::getType

(mongodb >=1.0.0)

MongoDBBSONBinary::getType — Повертає тип Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::getType(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тип Binary.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONBinary::getType()****

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getType());

?>
```

Результат виконання цього прикладу:

```
int(0)
```

### Дивіться також

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)