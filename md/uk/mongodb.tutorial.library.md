---
navigation:
  - mongodb.tutorial.md: '" Навчальні матеріали'
  - mongodb.tutorial.apm.md: >-
      Моніторинг продуктивності програми (Application Performance Monitoring або
      APM) »
  - index.md: PHP Manual
  - mongodb.tutorial.md: Навчальні матеріали
title: Робота бібліотеки PHP із драйвером MongoDB (PHPLIB)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Робота бібліотеки PHP із драйвером MongoDB (PHPLIB)

Після початкового налаштування драйвера продовжиться пояснення того, як розпочати роботу з драйвером MongoDB та користувальницькою бібліотекою, щоб створити перший проект.

## Встановлення бібліотеки PHP через Composer

Останнє, що необхідно встановити перед тим, як почати писати програму, це бібліотека PHP.

Бібліотеку встановлюватимемо через пакетний менеджер [» Composer](https://getcomposer.org/). Інструкції зі встановлення Composer на різні платформи опубліковані на його сайті.

Бібліотеку встановлюють так:

$ composer require mongodb/mongodb

Буде виведено щось на кшталт:

./composer.json has been created Loading composer repositories with package information Updating dependencies (including require-dev)

-   Installing mongodb/mongodb (1.0.0) Downloading: 100%

Writing lock file Generating autoload files

Composer створить кілька файлів: `composer.json` `composer.lock` та директорію `vendor`, що містить саму бібліотеку та інші залежності, які будуть потрібні в проекті.

## Робота з бібліотекою PHP

Крім управління залежностями, Composer також містить автозавантажувач класів цих залежностей. Необхідно переконатися, що цей автозавантажувач включений у початок скрипту або код початкового завантаження програми:

```php
<?php
// Этот путь должен указывать на автозагрузчик Composer
require 'vendor/autoload.php';
```

Після цього можна використовувати бібліотеку як описано [» в документації](https://www.mongodb.com/docs/php-library/current/)

Якщо раніше доводилося працювати з драйвером MongoDB іншими мовами, API бібліотеки буде виглядати знайомим. Він містить клас [» Client](https://www.mongodb.com/docs/php-library/master/reference/class/MongoDBClient/)для соединения с MongoDB, класс[» Database](https://www.mongodb.com/docs/php-library/master/reference/class/MongoDBDatabase/) для операцій рівня бази даних (наприклад, команди, керування колекціями) та клас [» Collection](https://www.mongodb.com/docs/php-library/master/reference/class/MongoDBCollection)для операций уровня коллекций (наПриклад, операций[» CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete), Управління індексами).

Наприклад, ось як вставити документ у колекцію *beers* бази даних *demo* :

```php
<?php
require 'vendor/autoload.php'; // подключаем автозагрузчик классов Composer

$client = new MongoDB\Client("mongodb://localhost:27017");
$collection = $client->demo->beers;

$result = $collection->insertOne( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );

echo "Идентификатор вставленного документа '{$result->getInsertedId()}'";
?>
```

Оскільки вставлений документ не містив поля `_id`драйвер згенерує для сервера об'єкт [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md), щоб використовувати як `_id`. Це значення також стає доступним методу, що викликається на об'єкті результату `insertOne`

Після вставки можна запросити щойно вставлені дані. Для цього викликають метод `find`, який повертає курсор, що ітерується:

```php
<?php
require 'vendor/autoload.php'; // подключаем автозагрузчик классов Composer

$client = new MongoDB\Client("mongodb://localhost:27017");
$collection = $client->demo->beers;

$result = $collection->find( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );

foreach ($result as $entry) {
    echo $entry['_id'], ': ', $entry['name'], "\n";
}
?>
```

Хоча після знайомства з прикладами може бути неочевидно, але документи BSON і масиви за умовчанням десеріалізовані як типи класів у бібліотеці. Ці класи дають гарантію, що значення збережуть типи при серіалізації назад у BSON, що унеможливлює проблеми зі старими драйверами, коли масиви могли перетворитися на документи і навпаки. А також цей тип класів розширює клас [ArrayObject](class.arrayobject.md)що підвищує зручність роботи з ними. Докладніше про серіалізацію та десеріалізацію між змінними PHP та BSON розказано у специфікації [Постійні дані](mongodb.persistence.md)
