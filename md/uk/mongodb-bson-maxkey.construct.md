Конструктор MaxKey

-   [« MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.html)
    
-   [MongoDB\\BSON\\MaxKey::jsonSerialize »](mongodb-bson-maxkey.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.html)
    
-   Конструктор MaxKey
    

# MongoDBBSONMaxKey::construct

(mongodb >=1.0.0)

MongoDBBSONMaxKey::construct — Конструктор MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::__construct()
```

### Список параметрів

Ця функція не має параметрів.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONMaxKey::construct()****

```php
<?php

var_dump(new MongoDB\BSON\MaxKey());

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\BSON\MaxKey)#1 (0) {
}
```

### Дивіться також

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)