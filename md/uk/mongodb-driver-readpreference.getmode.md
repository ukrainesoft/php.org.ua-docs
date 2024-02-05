---
navigation:
  - mongodb-driver-readpreference.getmaxstalenessseconds.md: '« MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds'
  - mongodb-driver-readpreference.getmodestring.md: 'MongoDB\\Driver\\ReadPreference::getModeString »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::getMode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::getMode

(mongodb >=1.0.0)

MongoDB\\Driver\\ReadPreference::getMode — Повертає "mode" ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getMode(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає параметр "mode" ReadPreference

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\ReadPreference::getMode()\*\*\*\*

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_NEAREST);
var_dump($rp->getMode());

?>
```

Результат виконання наведеного прикладу:

```
int(1)
int(5)
int(2)
int(6)
int(10)
```

### Дивіться також

-   [MongoDB\\Driver\\ReadPreference::getModeString()](mongodb-driver-readpreference.getmodestring.md) - Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка
-   [» Посібник з переваги читання](https://www.mongodb.com/docs/manual/core/read-preference/)
