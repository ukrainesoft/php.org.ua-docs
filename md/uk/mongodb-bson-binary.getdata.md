Повертає дані Binary

-   [« MongoDB\\BSON\\Binary::\_\_construct](mongodb-bson-binary.construct.html)
    
-   [MongoDB\\BSON\\Binary::getType »](mongodb-bson-binary.gettype.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html)
    
-   Повертає дані Binary
    

# MongoDBBSONBinary::getData

(mongodb >=1.0.0)

MongoDBBSONBinary::getData — Повертає дані Binary

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::getData(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані Binary.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONBinary::getData()****

```php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getData());

?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
```

### Дивіться також

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)