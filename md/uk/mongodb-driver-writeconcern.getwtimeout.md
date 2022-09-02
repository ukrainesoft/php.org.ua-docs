---
navigation:
  - mongodb-driver-writeconcern.getw.md: '« MongoDBDriverWriteConcern::getW'
  - mongodb-driver-writeconcern.isdefault.md: 'MongoDBDriverWriteConcern::isDefault »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDBDriverWriteConcern
title: 'MongoDBDriverWriteConcern::getWtimeout'
---
# MongoDBDriverWriteConcern::getWtimeout

(mongodb >=1.0.0)

MongoDBDriverWriteConcern::getWtimeout — Повертає опцію "wtimeout" WriteConcern

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::getWtimeout(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "wtimeout" WriteConcern.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.7.0 | У 32-розрядних системах метод завжди буде усікати значення `wTimeout`якщо воно виходить за межі 32-бітного діапазону. У цьому випадку буде видано попередження. |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcern::getWtimeout()****

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getWtimeout());

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 3000);
var_dump($wc->getWtimeout());

?>
```

Результат виконання цього прикладу:

```
int(0)
int(3000)
```

### Дивіться також

-   [» Руководство по гарантии записи](https://www.mongodb.com/docs/manual/reference/write-concern/)
