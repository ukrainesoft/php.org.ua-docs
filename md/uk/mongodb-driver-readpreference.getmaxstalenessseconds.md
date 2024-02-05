---
navigation:
  - mongodb-driver-readpreference.gethedge.md: '« MongoDB\\Driver\\ReadPreference::getHedge'
  - mongodb-driver-readpreference.getmode.md: 'MongoDB\\Driver\\ReadPreference::getMode »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds

(mongodb >=1.2.0)

MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds — Повертає параметр "maxStalenessSeconds" ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getMaxStalenessSeconds(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає параметр "maxStalenessSeconds" ReadPreference. Якщо не вказано максимальну staleness, повертається **`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds()\*\*\*\*

```php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => MongoDB\Driver\ReadPreference::NO_MAX_STALENESS,
]);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS,
]);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => 1000,
]);
var_dump($rp->getMaxStalenessSeconds());

?>
```

Результат виконання наведеного прикладу:

```
int(-1)
int(-1)
int(90)
int(1000)
```

### Дивіться також

-   [» Посібник з переваги читання](https://www.mongodb.com/docs/manual/core/read-preference/)
