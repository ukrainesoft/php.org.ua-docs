Повертає прапори Regex

-   [« MongoDBBSONRegex::construct](mongodb-bson-regex.construct.html)
    
-   [MongoDBBSONRegex::getPattern »](mongodb-bson-regex.getpattern.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONRegex](class.mongodb-bson-regex.html)
    
-   Повертає прапори Regex
    

# MongoDBBSONRegex::getFlags

(mongodb >=1.0.0)

MongoDBBSONRegex::getFlags — Повертає прапори Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::getFlags(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає прапори Regex.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONRegex::getFlags()****

```php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump($regex->getFlags());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "i"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [» Підтримувані прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)