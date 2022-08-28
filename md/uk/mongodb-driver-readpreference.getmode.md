Повертає параметр "mode" ReadPreference

-   [« MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds](mongodb-driver-readpreference.getmaxstalenessseconds.html)
    
-   [MongoDB\\Driver\\ReadPreference::getModeString »](mongodb-driver-readpreference.getmodestring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)
    
-   Повертає параметр "mode" ReadPreference
    

# MongoDBDriverReadPreference::getMode

(mongodb >=1.0.0)

MongoDBDriverReadPreference::getMode — Повертає "mode" ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getMode(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає параметр "mode" ReadPreference

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadPreference::getMode()****

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_NEAREST);
var_dump($rp->getMode());

?>
```

Результат виконання цього прикладу:

```
int(1)
int(5)
int(2)
int(6)
int(10)
```

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference::getModeString()](mongodb-driver-readpreference.getmodestring.html) - Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка
-   [» Руководство по предпочтению чтения](https://www.mongodb.com/docs/manual/core/read-preference/)