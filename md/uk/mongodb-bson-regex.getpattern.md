Повертає шаблон Regex

-   [« MongoDB\\BSON\\Regex::getFlags](mongodb-bson-regex.getflags.html)
    
-   [MongoDB\\BSON\\Regex::jsonSerialize »](mongodb-bson-regex.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html)
    
-   Повертає шаблон Regex
    

# MongoDBBSONRegex::getPattern

(mongodb >=1.0.0)

MongoDBBSONRegex::getPattern — Повертає шаблон Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::getPattern(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шаблон Regex.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONRegex::getPattern()****

```php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump($regex->getPattern());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "regex"
```

### Дивіться також

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)