---
navigation:
  - mongodb-driver-readconcern.construct.md: '« MongoDB\\Driver\\ReadConcern::\_\_construct'
  - mongodb-driver-readconcern.isdefault.md: 'MongoDB\\Driver\\ReadConcern::isDefault »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern
title: 'MongoDB\\Driver\\ReadConcern::getLevel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadConcern::getLevel

(mongodb >=1.0.0)

MongoDB\\Driver\\ReadConcern::getLevel — Повертає опцію "level" ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::getLevel(): ?string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "level" ReadConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\ReadConcern::getLevel()\*\*\*\*

```php
<?php

$rc = new MongoDB\Driver\ReadConcern();
var_dump($rc->getLevel());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->getLevel());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);
var_dump($rc->getLevel());

?>
```

Результат виконання наведеного прикладу:

```
NULL
string(5) "local"
string(8) "majority"
```

### Дивіться також

-   [» Довідка за гарантіями читання](https://www.mongodb.com/docs/manual/reference/read-concern/)
