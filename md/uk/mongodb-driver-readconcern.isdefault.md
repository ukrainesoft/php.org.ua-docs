---
navigation:
  - mongodb-driver-readconcern.getlevel.html: '« MongoDBDriverReadConcern::getLevel'
  - mongodb-driver-readconcern.serialize.html: 'MongoDBDriverReadConcern::serialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-readconcern.html: MongoDBDriverReadConcern
title: 'MongoDBDriverReadConcern::isDefault'
---
# MongoDBDriverReadConcern::isDefault

(mongodb >=1.3.0)

MongoDBDriverReadConcern::isDefault — Перевіряє, чи є гарантією читання за умовчанням

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadConcern::isDefault(): bool
```

Повертає, чи це гарантія читання за замовчуванням (тобто параметри не вказані). Цей метод в першу чергу призначений для використання у поєднанні з [MongoDBDriverManager::getReadConcern()](mongodb-driver-manager.getreadconcern.md), щоб визначити, чи був побудований Manager без будь-яких гарантій читання.

Драйвер не буде включати гарантії читання за умовчанням у своїх операціях читання (наприклад, [MongoDBDriverManager::executeQuery()](mongodb-driver-manager.executequery.md)), щоб сервер міг застосовувати власні значення за замовчуванням. Бібліотеки, які звертаються до гарантій читання Manager, щоб включити його у власні команди читання, повинні використовувати цей метод, щоб гарантувати, що гарантії читання за замовчуванням залишаються невстановленими.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо це гарантії читання за умовчанням, та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverReadConcern::isDefault()****

```php
<?php

$rc = new MongoDB\Driver\ReadConcern(null);
var_dump($rc->isDefault());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);
var_dump($rc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/?readConcernLevel=majority');
$rc = $manager->getReadConcern();
var_dump($rc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/');
$rc = $manager->getReadConcern();
var_dump($rc->isDefault());

?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [MongoDBDriverManager::getReadConcern()](mongodb-driver-manager.getreadconcern.md) - Повертає ReadConcern для Manager
-   [» Справка по гарантиям чтения](https://www.mongodb.com/docs/manual/reference/read-concern/)
