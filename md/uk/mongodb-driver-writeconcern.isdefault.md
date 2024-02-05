---
navigation:
  - mongodb-driver-writeconcern.getwtimeout.md: '« MongoDB\\Driver\\WriteConcern::getWtimeout'
  - mongodb-driver-writeconcern.serialize.md: 'MongoDB\\Driver\\WriteConcern::serialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-writeconcern.md: MongoDB\\Driver\\WriteConcern
title: 'MongoDB\\Driver\\WriteConcern::isDefault'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\WriteConcern::isDefault

(mongodb >=1.3.0)

MongoDB\\Driver\\WriteConcern::isDefault — Перевіряє, чи є гарантія запису за промовчанням

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::isDefault(): bool
```

Перевіряє, чи ця гарантія запису за промовчанням (тобто не вказані параметри). Цей метод в першу чергу призначений для використання спільно з [MongoDB\\Driver\\Manager::getWriteConcern()](mongodb-driver-manager.getwriteconcern.md) для визначення того, чи об'єкт Manager був створений без будь-яких опцій гарантії запису.

Драйвер не включатиме гарантію запису за замовчуванням у свої операції запису (наприклад, [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)), щоб дозволити серверу застосовувати свою власну за умовчанням, яка, можливо, була [» змінена](https://www.mongodb.com/docs/manual/core/replica-set-write-concern/#modify-default-write-concern). Бібліотеки, які звертаються до гарантії запису Manager, щоб увімкнути її у власні команди запису, повинні використовувати цей метод, щоб гарантувати, що гарантії запису за замовчуванням залишаються невстановленими.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо ця гарантія запису за замовчуванням, або **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\WriteConcern::isDefault()\*\*\*\*

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/?w=majority');
$wc = $manager->getWriteConcern();
var_dump($wc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/');
$wc = $manager->getWriteConcern();
var_dump($wc->isDefault());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::getWriteConcern()](mongodb-driver-manager.getwriteconcern.md) \- Повертає WriteConcern для Manager
-   [» Зміна гарантії запису за замовчуванням](https://www.mongodb.com/docs/manual/core/replica-set-write-concern/#modify-default-write-concern)у посібнику MongoDB
-   [» Довідкова інформація щодо гарантії запису](https://www.mongodb.com/docs/manual/reference/write-concern/)
