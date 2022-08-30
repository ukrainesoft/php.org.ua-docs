Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка

-   [« MongoDBDriverReadPreference::getMode](mongodb-driver-readpreference.getmode.html)
    
-   [MongoDBDriverReadPreference::getTagSets »](mongodb-driver-readpreference.gettagsets.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)
    
-   Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка
    

# MongoDBDriverReadPreference::getModeString

(mongodb >=1.7.0)

MongoDBDriverReadPreference::getModeString — Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getModeString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 **Приклад використання MongoDBDriverReadPreference::getModeString()****

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::PRIMARY);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::SECONDARY);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::NEAREST);
var_dump($rp->getModeString());

?>
```

Результат виконання цього прикладу:

```
string(7) "primary"
string(16) "primaryPreferred"
string(9) "secondary"
string(18) "secondaryPreferred"
string(7) "nearest"
```

### Дивіться також

-   [MongoDBDriverReadPreference::getMode()](mongodb-driver-readpreference.getmode.html) - Повертає параметр "mode" ReadPreference
-   [» Документация по Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)