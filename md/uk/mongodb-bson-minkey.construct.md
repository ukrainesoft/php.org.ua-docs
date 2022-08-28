Конструктор MinKey

-   [« MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html)
    
-   [MongoDB\\BSON\\MinKey::jsonSerialize »](mongodb-bson-minkey.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html)
    
-   Конструктор MinKey
    

# MongoDBBSONMinKey::construct

(mongodb >=1.0.0)

MongoDBBSONMinKey::construct — Конструктор MinKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::__construct()
```

### Список параметрів

Ця функція не має параметрів.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONMinKey::construct()****

```php
<?php

var_dump(new MongoDB\BSON\MinKey());

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\BSON\MinKey)#1 (0) {
}
```

### Дивіться також

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)