Повертає рядкову виставу Regex

-   [« MongoDBBSONRegex::serialize](mongodb-bson-regex.serialize.html)
    
-   [MongoDBBSONRegex::unserialize »](mongodb-bson-regex.unserialize.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONRegex](class.mongodb-bson-regex.html)
    
-   Повертає рядкову виставу Regex
    

# MongoDBBSONRegex::toString

(mongodb >=1.0.0)

MongoDBBSONRegex::toString — Повертає рядкову виставу Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::__toString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкову виставу Regex.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONRegex::toString()****

```php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump((string) $regex);

?>
```

Результат виконання цього прикладу:

```
string(8) "/regex/i"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)