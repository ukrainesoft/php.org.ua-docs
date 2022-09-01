---
navigation:
  - mongodb-bson-regex.getflags.html: '« MongoDBBSONRegex::getFlags'
  - mongodb-bson-regex.jsonserialize.html: 'MongoDBBSONRegex::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.html: MongoDBBSONRegex
title: 'MongoDBBSONRegex::getPattern'
---
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

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

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
