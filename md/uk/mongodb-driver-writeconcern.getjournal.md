---
navigation:
  - mongodb-driver-writeconcern.construct.md: '« MongoDB\\Driver\\WriteConcern::\_\_construct'
  - mongodb-driver-writeconcern.getw.md: 'MongoDB\\Driver\\WriteConcern::getW »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::getJournal'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::getJournal

(mongodb >=1.0.0)

MongoDB\\Driver\\WriteConcern::getJournal - Повертає опцію "journal" WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::getJournal(): ?bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "journal" WriteConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteConcern::getJournal()\*\*\*\*

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getJournal());

$wc = new MongoDB\Driver\WriteConcern(1, 0, true);
var_dump($wc->getJournal());

$wc = new MongoDB\Driver\WriteConcern(1, 0, false);
var_dump($wc->getJournal());

?>
```

Результат виконання наведеного прикладу:

```
NULL
bool(true)
bool(false)
```

### Дивіться також

-   [» Посібник з гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
