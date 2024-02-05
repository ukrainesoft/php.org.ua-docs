---
navigation:
  - mongodb-driver-readconcern.getlevel.md: '« MongoDB\\Driver\\ReadConcern::getLevel'
  - mongodb-driver-readconcern.serialize.md: 'MongoDB\\Driver\\ReadConcern::serialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.md: MongoDB\\Driver\\ReadConcern
title: 'MongoDB\\Driver\\ReadConcern::isDefault'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadConcern::isDefault

(mongodb >=1.3.0)

MongoDB\\Driver\\ReadConcern::isDefault — Перевіряє, чи є гарантією читання за умовчанням

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::isDefault(): bool
```

Повертає, чи це гарантія читання за замовчуванням (тобто параметри не вказані). Цей метод в першу чергу призначений для використання у поєднанні з [MongoDB\\Driver\\Manager::getReadConcern()](mongodb-driver-manager.getreadconcern.md), щоб визначити, чи був побудований Manager без будь-яких гарантій читання.

Драйвер не буде включати гарантії читання за умовчанням у своїх операціях читання (наприклад, [MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.md)), щоб сервер міг застосовувати власні значення за замовчуванням. Бібліотеки, які звертаються до гарантій читання Manager, щоб включити його у власні команди читання, повинні використовувати цей метод, щоб гарантувати, що гарантії читання за замовчуванням залишаються невстановленими.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо це гарантії читання за умовчанням, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\ReadConcern::isDefault()\*\*\*\*

```php
<?php

$rc = new MongoDB\Driver\ReadConcern(null);
var_dump($rc->isDefault());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);
var_dump($rc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/?readConcernLevel=majority');
$rc = $manager->getReadConcern();
var_dump($rc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/');
$rc = $manager->getReadConcern();
var_dump($rc->isDefault());

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::getReadConcern()](mongodb-driver-manager.getreadconcern.md) \- Повертає ReadConcern для Manager
-   [» Довідка за гарантіями читання](https://www.mongodb.com/docs/manual/reference/read-concern/)
