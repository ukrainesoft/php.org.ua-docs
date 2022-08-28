Повертає опцію "journal" WriteConcern

-   [« MongoDB\\Driver\\WriteConcern::\_\_construct](mongodb-driver-writeconcern.construct.html)
    
-   [MongoDB\\Driver\\WriteConcern::getW »](mongodb-driver-writeconcern.getw.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)
    
-   Повертає опцію "journal" WriteConcern
    

# MongoDBDriverWriteConcern::getJournal

(mongodb >=1.0.0)

MongoDBDriverWriteConcern::getJournal - Повертає опцію "journal" WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::getJournal(): ?bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "journal" WriteConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcern::getJournal()****

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getJournal());

$wc = new MongoDB\Driver\WriteConcern(1, 0, true);
var_dump($wc->getJournal());

$wc = new MongoDB\Driver\WriteConcern(1, 0, false);
var_dump($wc->getJournal());

?>
```

Результат виконання цього прикладу:

```
NULL
bool(true)
bool(false)
```

### Дивіться також

-   [» Руководство по гарантии записи](https://www.mongodb.com/docs/manual/reference/write-concern/)