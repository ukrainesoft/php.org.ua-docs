Перевіряє, чи є гарантія запису за замовчуванням

-   [« MongoDB\\Driver\\WriteConcern::getWtimeout](mongodb-driver-writeconcern.getwtimeout.html)
    
-   [MongoDB\\Driver\\WriteConcern::serialize »](mongodb-driver-writeconcern.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)
    
-   Перевіряє, чи є гарантія запису за замовчуванням
    

# MongoDBDriverWriteConcern::isDefault

(mongodb >=1.3.0)

MongoDBDriverWriteConcern::isDefault — Перевіряє, чи є гарантія запису за промовчанням

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteConcern::isDefault(): bool
```

Перевіряє, чи ця гарантія запису за промовчанням (тобто не вказані параметри). Цей метод в першу чергу призначений для використання спільно з [MongoDB\\Driver\\Manager::getWriteConcern()](mongodb-driver-manager.getwriteconcern.html) для визначення того, чи об'єкт Manager був створений без будь-яких опцій гарантії запису.

Драйвер не включатиме гарантію запису за замовчуванням у свої операції запису (наприклад, [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html)), щоб дозволити серверу застосовувати свою власну за умовчанням, яка, можливо, була [» изменена](https://www.mongodb.com/docs/manual/core/replica-set-write-concern/#modify-default-write-concern). Бібліотеки, які звертаються до гарантії запису Manager, щоб включити її у власні команди запису, повинні використовувати цей метод, щоб гарантувати, що гарантії запису за замовчуванням залишаються невстановленими.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо ця гарантія запису за промовчанням, або **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverWriteConcern::isDefault()****

```php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/?w=majority');
$wc = $manager->getWriteConcern();
var_dump($wc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/');
$wc = $manager->getWriteConcern();
var_dump($wc->isDefault());

?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::getWriteConcern()](mongodb-driver-manager.getwriteconcern.html) - Повертає WriteConcern для Manager
-   [» Изменение гарантии записи по умолчанию](https://www.mongodb.com/docs/manual/core/replica-set-write-concern/#modify-default-write-concern) у посібнику MongoDB
-   [» Справочная информация по гарантии записи](https://www.mongodb.com/docs/manual/reference/write-concern/)