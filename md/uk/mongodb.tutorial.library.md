Використання бібліотеки PHP для MongoDB (PHPLIB)

-   [" Навчальні матеріали](mongodb.tutorial.html)
    
-   [Моніторинг продуктивності програми (Application Performance Monitoring або APM) »](mongodb.tutorial.apm.html)
    
-   [PHP Manual](index.html)
    
-   [Навчальні матеріали](mongodb.tutorial.html)
    
-   Використання бібліотеки PHP для MongoDB (PHPLIB)
    

# Використання бібліотеки PHP для MongoDB (PHPLIB)

Після початкового налаштування драйвера, ми продовжимо пояснювати, як почати роботу з драйвером MongoDB і відповідною бібліотекою користувача, для створення нашого першого проекту.

## Встановлення бібліотеки PHP за допомогою Composer

Останнє, що нам необхідно встановити, перш ніж почати писати нашу програму - встановити бібліотеку PHP.

Бібліотеку встановлюватимемо за допомогою пакетного менеджера [» Composer](https://getcomposer.org/). Інструкції зі встановлення Composer шукайте на його сайті.

Встановлюємо бібліотеку так:

$ composer require mongodb/mongodb

Буде виведено щось на кшталт:

./composer.json has been created Loading composer repositories with package information Updating dependencies (including require-dev)

-   Installing mongodb/mongodb (1.0.0) Downloading: 100%

Writing lock file Generating autoload files

Composer створить кілька файлів: `composer.json` `composer.lock` та директорію `vendor`, що містить саму бібліотеку та інші залежності, які будуть потрібні у вашому проекті.

## Використання бібліотеки PHP

Крім управління залежностями, Composer також надає автопідвантажувач класів для цих залежностей. Переконайтеся, що ви включили цей автозавантажувач на початок свого скрипта або в код bootstrap() вашої програми:

```php
<?php
// Этот путь должен указывать на автозагрузчик Composer
require 'vendor/autoload.php';
```

Після цього можна використовувати будь-який функціонал, описаний у [» документации по библиотеке](https://www.mongodb.com/docs/php-library/current/)

Якщо ви раніше використовували старіший драйвер (тобто модуль `mongo`), то API бібліотеки має бути вам знайоме. Воно містить клас [» Client](https://www.mongodb.com/docs/php-library/master/reference//class/MongoDBClient/) для з'єднання з MongoDB, клас [» Database](https://www.mongodb.com/docs/php-library/master/reference//class/MongoDBDatabase/) для операцій рівня бази даних (тобто команди, управління колекціями) та клас [» Collection](https://www.mongodb.com/docs/php-library/master/reference//class/MongoDBCollection) для операцій рівня колекції (тобто методи [» CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete), Управління індексами). Різні методи Collection були перейменовані для більшої зрозумілості та відповідності мовно-незалежній [» специфікації](https://github.com/mongodb/specifications/blob/master/source/crud/crud.rst)

Приклад, як вставити документ у колекцію *beers* бази даних *demo*

```php
<?php
require 'vendor/autoload.php'; // подключаем автоподгрузчик классов Composer

$client = new MongoDB\Client("mongodb://localhost:27017");
$collection = $client->demo->beers;

$result = $collection->insertOne( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );

echo "Идентификатор вставленного документа '{$result->getInsertedId()}'";
?>
```

Замість ін'єкції згенерованого поля `_id` у вхідний документ (як це робилося у старих версіях драйвера), тепер можна це робити за допомогою методу `insertOne` повернутий об'єкт.

Після вставки ви, звичайно, можете запросити щойно вставлені дані. Для цього використовуйте метод `find`, який повертає курсор, що ітерується:

```php
<?php
require 'vendor/autoload.php'; // подключаем автоподгрузчик классов Composer

$client = new MongoDB\Client("mongodb://localhost:27017");
$collection = $client->demo->beers;

$result = $collection->find( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );

foreach ($result as $entry) {
    echo $entry['_id'], ': ', $entry['name'], "\n";
}
?>
```

Хоча з прикладу це не очевидно, але документи BSON і масиви за умовчанням десеріалізовані як типи класів у бібліотеці. Ці класи гарантують, що значення збережуть свої типи коли серіалізуватимуться назад у BSON, що дозволяє уникнути проблеми старих драйверів, коли масиви могли перетворитися на документи і навпаки. Крім того, класи успадковують [ArrayObject](class.arrayobject.html) для більшої зручності використання. Більш детально про серіалізацію та десеріалізацію між змінними PHP і BSON можна прочитати у специфікації [Постійні дані](mongodb.persistence.html)