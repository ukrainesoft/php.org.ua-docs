---
navigation:
  - mongodb-driver-readpreference.getmode.md: '« MongoDB\\Driver\\ReadPreference::getMode'
  - mongodb-driver-readpreference.gettagsets.md: 'MongoDB\\Driver\\ReadPreference::getTagSets »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::getModeString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::getModeString

(mongodb >=1.7.0)

MongoDB\\Driver\\ReadPreference::getModeString — Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getModeString(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1**Приклад використання MongoDB\\Driver\\ReadPreference::getModeString()\*\*\*\*

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::PRIMARY);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::SECONDARY);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::NEAREST);
var_dump($rp->getModeString());

?>
```

Результат виконання наведеного прикладу:

```
string(7) "primary"
string(16) "primaryPreferred"
string(9) "secondary"
string(18) "secondaryPreferred"
string(7) "nearest"
```

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference::getMode()](mongodb-driver-readpreference.getmode.md) - Повертає параметр "mode" ReadPreference
-   [» Документація з Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)
