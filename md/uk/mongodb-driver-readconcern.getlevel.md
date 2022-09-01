---
navigation:
  - mongodb-driver-readconcern.construct.html: '« MongoDBDriverReadConcern::construct'
  - mongodb-driver-readconcern.isdefault.html: 'MongoDBDriverReadConcern::isDefault »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.html: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::getLevel'
---
# MongoDBDriverReadConcern::getLevel

(mongodb >=1.0.0)

MongoDBDriverReadConcern::getLevel — Повертає опцію "level" ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::getLevel(): ?string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "level" ReadConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadConcern::getLevel()****

```php
<?php

$rc = new MongoDB\Driver\ReadConcern();
var_dump($rc->getLevel());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->getLevel());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);
var_dump($rc->getLevel());

?>
```

Результат виконання цього прикладу:

```
NULL
string(5) "local"
string(8) "majority"
```

### Дивіться також

-   [» Справка по гарантиям чтения](https://www.mongodb.com/docs/manual/reference/read-concern/)
