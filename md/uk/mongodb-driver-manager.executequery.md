- [« MongoDB\Driver\Manager::executeCommand](mongodb-driver-manager.executecommand.md)
- [MongoDB\Driver\Manager::executeReadCommand »](mongodb-driver-manager.executereadcommand.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Manager](class.mongodb-driver-manager.md)
- Виконує запит до бази даних

# MongoDB\Driver\Manager::executeQuery

(mongodb \>=1.0.0)

MongoDB\Driver\Manager::executeQuery — Виконує запит до бази даних

### Опис

final public **MongoDB\Driver\Manager::executeQuery**(string
`$namespace`, [MongoDB\Driver\Query](class.mongodb-driver-query.md)
`$query`, array `$options` = array()):
[MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)

Вибирає сервер відповідно до опції ``readPreference'` і виконує
запит на цьому сервері. За замовчуванням використовуватиметься перевага
читання з URI [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri).

### Список параметрів

`namespace` (string)
Повністю певне ім'я (тобто `databaseName.collectionName`).

`query` ([MongoDB\Driver\Query](class.mongodb-driver-query.md))
Запит на виконання.

`options`
| Опція          | Тип                                                                     | Опис                                                                             |
| -------------- | ----------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| readPreference | [MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md) | Перевага читання, що використовується для вибору сервера для виконання операції. |
| session        | [MongoDB\Driver\Session](class.mongodb-driver-session.md)               | Сесія зв'язування з операцією.                                                   |

**options**

### Значення, що повертаються

У разі успішного виконання повертає
[MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md).

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).
- При невдалому з'єднанні з сервером (крім помилок автентифікації),
кидає виняток
[MongoDB\Driver\Exception\ConnectionException](class.mongodb-driver-exception-connectionexception.md).
- За невдалої аутентифікації кидає виняток
[MongoDB\Driver\Exception\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md).
- У разі виникнення інших помилок (наприклад, неправильні оператори
запиту), викидає виняток
[MongoDB\Driver\Exception\RuntimeException](class.mongodb-driver-exception-runtimeexception.md).

### Список змін

| Версія             | Опис                                                                                                                                                                           |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом options. Для зворотної сумісності цей параметр все одно прийме об'єкт [MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md). |

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\Manager::executeQuery()****

` <?php$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['x' => 1]) ;$bulk->insert(['x' => 2]);$bulk->insert(['x' => 3]);$manager->executeBulkWrite('db.collection', $bulk);$ filter ='['x' => ['$gt' => 1]];$options = [    'projection' => ['_id' => 0],    'sort' => ['x' ],];$query = new MongoDB\Driver\Query($filter, $options);$cursor = $manager->executeQuery('db.collection', $query);foreach ($cursor as $document) { ($document);}?> `

Результат виконання цього прикладу:

object(stdClass)#6 (1) {
["x"]=>
int(3)
}
object(stdClass)#7 (1) {
["x"]=>
int(2)
}

**Приклад #2 Обмеження часу виконання запиту**

Опція ``maxTimeMS'` класу
[MongoDB\Driver\Query](class.mongodb-driver-query.md) може
використовуватись для обмеження часу виконання запиту. Зверніть
увагу, що цей термін застосовується на стороні сервера та не враховує
затримки мережі. Дивіться [» Завершення виконання операцій](https://www.mongodb.com/docs/manual/tutorial/terminate-running-operations/#maxtimems)
у посібнику MongoDB для отримання додаткової інформації.

` <?php$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');$filter = ['x' => ['$gt' => 1]];$options = [    '' maxTimeMS' => 1000,];$query = new MongoDB\Driver\Query($filter, $options);$cursor = $manager->executeQuery('db.collection', $query);foreach ($cursor document) {   var_dump($document);}?> `

Якщо запит не завершиться через секунду після початку виконання на
сервері, буде викинуто виняток
[MongoDB\Driver\Exception\ExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.md).

### Дивіться також

- [MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)
- [MongoDB\Driver\Query](class.mongodb-driver-query.md)
- [MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md)
- [MongoDB\Driver\Server::executeQuery()](mongodb-driver-server.executequery.md) -
Виконує запит до бази даних на сервері
