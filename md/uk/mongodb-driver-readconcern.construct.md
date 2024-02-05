---
navigation:
  - mongodb-driver-readconcern.bsonserialize.md: '« MongoDB\\Driver\\ReadConcern::bsonSerialize'
  - mongodb-driver-readconcern.getlevel.md: 'MongoDB\\Driver\\ReadConcern::getLevel »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern
title: 'MongoDB\\Driver\\ReadConcern::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadConcern::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\ReadConcern::\_\_construct — Створює новий ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::__construct(?string $level = null)
```

Створює новий [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)що є об'єктом незмінного значення.

### Список параметрів

`level`

[» Рівень гарантій читання](https://www.mongodb.com/docs/manual/reference/read-concern/#read-concern-levels). Ви можете використовувати, але не обмежуючись цим, одну з [констант класу](class.mongodb-driver-readconcern.md#mongodb-driver-readconcern.constants)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\Driver\\ReadConcern::\_\_construct()\*\*\*\*

```php
<?php

/* Неуказанный уровень изоляции чтения (использует поведение сервера по умолчанию) */
$rc = new MongoDB\Driver\ReadConcern();

/* Запрашиваем изоляцию чтения от одного узла набора реплик */
$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);

/* Запрашиваем изоляцию чтения от большинства узлов набора реплик */
$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);

?>
```

### Дивіться також

-   [» Довідка за гарантіями читання](https://www.mongodb.com/docs/manual/reference/read-concern/)
