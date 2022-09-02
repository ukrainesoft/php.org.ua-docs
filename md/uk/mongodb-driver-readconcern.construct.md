---
navigation:
  - mongodb-driver-readconcern.bsonserialize.md: '« MongoDBDriverReadConcern::bsonSerialize'
  - mongodb-driver-readconcern.getlevel.md: 'MongoDBDriverReadConcern::getLevel »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::construct'
---
# MongoDBDriverReadConcern::construct

(mongodb >=1.0.0)

MongoDBDriverReadConcern::construct — Створює новий ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::__construct(?string $level = null)
```

Створює новий [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md)що є об'єктом незмінного значення.

### Список параметрів

`level`

[» Рівень гарантій читання](https://www.mongodb.com/docs/manual/reference/read-concern/#read-concern-levels). Ви можете використовувати, але не обмежуючись цим, одну з [констант класса](class.mongodb-driver-readconcern.md#mongodb-driver-readconcern.constants)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadConcern::construct()****

```php
<?php

/* Неуказанный уровень изоляции чтения (использует поведение сервера по умолчанию) */
$rc = new MongoDB\Driver\ReadConcern();

/* Запрашиваем изоляцию чтения от одного узла набора реплик */
$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);

/* Запрашиваем изоляцию чтения от большинства узлов набора реплик */
$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);

?>
```

### Дивіться також

-   [» Справка по гарантиям чтения](https://www.mongodb.com/docs/manual/reference/read-concern/)
