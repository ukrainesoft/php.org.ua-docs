---
navigation:
  - mongodb-driver-writeconcern.getjournal.md: '« MongoDB\\Driver\\WriteConcern::getJournal'
  - mongodb-driver-writeconcern.getwtimeout.md: 'MongoDB\\Driver\\WriteConcern::getWtimeout »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::getW'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::getW

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteConcern::getW — Повертає опцію "w" WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::getW(): string|int|null
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "w" WriteConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteConcern::getW()\*\*\*\*

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getW());

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY);
var_dump($wc->getW());

?>
```

Результат виконання наведеного прикладу:

```
int(1)
string(8) "majority"
```

### Дивіться також

-   [» Посібник з гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
