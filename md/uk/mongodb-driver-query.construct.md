- [«MongoDB\Driver\Query](class.mongodb-driver-query.md)
- [MongoDB\Driver\BulkWrite »](class.mongodb-driver-bulkwrite.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Query](class.mongodb-driver-query.md)
- Створює новий запит

# MongoDB\Driver\Query::\_\_construct

(mongodb \>=1.0.0)

MongoDB\Driver\Query::\_\_construct — Створює новий запит

### Опис

final public **MongoDB\Driver\Query::\_\_construct**(array\|object
`$filter`, array `$queryOptions` = ?)

Створює новий [MongoDB\Driver\Query](class.mongodb-driver-query.md),
який є об'єктом незмінного значення, що представляє запит
до бази даних. Потім запит може бути виконаний за допомогою
[MongoDB\Driver\Manager::executeQuery()](mongodb-driver-manager.executequery.md).

### Список параметрів

`filter` (array\|object)
[» Предикат запиту](https://www.mongodb.com/docs/manual/tutorial/query-documents/).
Порожній предикат збігатиметься з усіма елементами колекції.

> **Примітка**: При обчисленні критеріїв запиту MongoDB порівнює
> типи та значення відповідно до власних [» правил порівняння
> типів > BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/),
> відмінних від правил [порівняння](types.comparisons.md) та [приведення > типів](language.types.type-juggling.md) PHP. Коли використовується
> спеціальний тип BSON, критерію запиту має відповідати [класу > BSON](book.bson.md) (тобто використовувати
> [MongoDB\BSON\ObjectId](class.mongodb-bson-objectid.md) для вибірки
> по
> [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)).

`queryOptions`
[TABLE]

**queryOptions**

### Помилки

- При помилці парсингу аргумент кидає виняток [MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Список змін

[TABLE]

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\Query::\_\_construct()****

` <?php/* Выберите только документы, автором которых является "bjori" с не менее 100 просмотров */$filter = [    'author' => 'bjori',    'views' => [        '$gte' => 100, ],];$options = [    /* Вернуть только следующие поля в соответствующих документах */    'projection' => [        'title' => 1,        'article' => 1,    ],    /* Вернуть документы в порядке убывания просмотров * /   'sort' => [       'views' => -1    ],];$query = new MongoDB\Driver\Query($filter, $options);$mana localhost:27017');$readPreference = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);$cursor = $manager->executeQuery('databaseName.collectionName', $query, $ $cursor as $document) {    var_dump($document);}?> `

### Дивіться також

- [MongoDB\Driver\Manager::executeQuery()](mongodb-driver-manager.executequery.md) -
Виконує запит до бази даних
- [MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)
