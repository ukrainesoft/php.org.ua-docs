---
navigation:
  - mongodb-driver-readconcern.bsonserialize.html: '« MongoDBDriverReadConcern::bsonSerialize'
  - mongodb-driver-readconcern.getlevel.html: 'MongoDBDriverReadConcern::getLevel »'
  - index.html: PHP Manual
  - class.mongodb-driver-readconcern.html: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::construct'
---
# MongoDBDriverReadConcern::construct

(mongodb >=1.0.0)

MongoDBDriverReadConcern::construct — Створює новий ReadConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::__construct(?string $level = null)
```

Створює новий [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html)що є об'єктом незмінного значення.

### Список параметрів

`level`

[» Рівень гарантій читання](https://www.mongodb.com/docs/manual/reference/read-concern/#read-concern-levels). Ви можете використовувати, але не обмежуючись цим, одну з [констант класса](class.mongodb-driver-readconcern.html#mongodb-driver-readconcern.constants)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

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
