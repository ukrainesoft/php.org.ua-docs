Повертає дані Binary

-   [« MongoDB\\BSON\\Binary::serialize](mongodb-bson-binary.serialize.html)
    
-   [MongoDB\\BSON\\Binary::unserialize »](mongodb-bson-binary.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)
    
-   Повертає дані Binary
    

# MongoDBBSONBinary::toString

(mongodb >=1.2.0)

MongoDBBSONBinary::toString — Повертає дані Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::__toString(): string
```

Цей метод є псевдонімом: [MongoDB\\BSON\\Binary::getData()](mongodb-bson-binary.getdata.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані Binary.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONBinary::toString()****

```php
<?php

var_dump((string) new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC));

?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
```

### Дивіться також

-   [MongoDB\\BSON\\Binary::getData()](mongodb-bson-binary.getdata.html) - Повертає дані Binary
-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)