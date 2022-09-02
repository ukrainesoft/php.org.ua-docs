---
navigation:
  - mongodb-driver-writeconcern.getjournal.md: '« MongoDBDriverWriteConcern::getJournal'
  - mongodb-driver-writeconcern.getwtimeout.md: 'MongoDBDriverWriteConcern::getWtimeout »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDBDriverWriteConcern
title: 'MongoDBDriverWriteConcern::getW'
---
# MongoDBDriverWriteConcern::getW

(mongodb >=1.0.0)

MongoDBDriverWriteConcern::getW — Повертає опцію "w" WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::getW(): string|int|null
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "w" WriteConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcern::getW()****

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getW());

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY);
var_dump($wc->getW());

?>
```

Результат виконання цього прикладу:

```
int(1)
string(8) "majority"
```

### Дивіться також

-   [» Руководство по гарантии записи](https://www.mongodb.com/docs/manual/reference/write-concern/)
