---
navigation:
  - mongodb-driver-manager.executebulkwrite.html: '« MongoDBDriverManager::executeBulkWrite'
  - mongodb-driver-manager.executequery.html: 'MongoDBDriverManager::executeQuery »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.html: MongoDBDriverManager
title: 'MongoDBDriverManager::executeCommand'
---
# MongoDBDriverManager::executeCommand

(mongodb >=1.0.0)

MongoDBDriverManager::executeCommand — Виконує команду бази даних

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeCommand(string $db, MongoDB\Driver\Command $command, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
```

Вибирає сервер відповідно до опції `"readPreference"` та виконує запит на цьому сервері. За промовчанням буде використовуватися перевага читання з URI [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

Цей метод не застосовує особливої ​​логіки до команди. Хоча цей метод приймає `"readConcern"` і `"writeConcern"`, які будуть включені в документи коанди, ці опції не будуть відповідати значенням за замовчуванням [MongoDB URI соединения](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri) , і не враховуватиметься версія сервера MongoDB. Тому користувачам рекомендується використовувати конкретні методи команди читання та/або запису, якщо це можливо.

### Список параметрів

`db` (string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDBDriverCommand](class.mongodb-driver-command.md)

Команда для виконання.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| readConcern | [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md) |  |
| Гарантія для застосування до операції. |  |  |

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference | [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | session | [MongoDBDriverSession](class.mongodb-driver-session.md)

Сесія зв'язування з операцією.

| | writeConcern | [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

**Увага**

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.md)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverCursor](class.mongodb-driver-cursor.md)

### Помилки

-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   У разі інших помилок (наприклад, неправильна команда), викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | Якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису, викидається виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. Для зворотної сумісності цей параметр все одно прийме об'єкт [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverManager::executeCommand()** з командою, яка повертає одиночний документ**

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$command = new MongoDB\Driver\Command(['ping' => 1]);

try {
    $cursor = $manager->executeCommand('admin', $command);
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}

/* Команда ping возвращает одиночный результат, поэтому мы должны получить доступ к
 * первому результату в курсор. */
$response = $cursor->toArray()[0];

var_dump($response);

?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["ok"]=>
  float(1)
}
```

**Приклад #2 Приклад використання **MongoDBDriverManager::executeCommand()** з командою, що повертає курсор**

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1, 'y' => 'foo']);
$bulk->insert(['x' => 2, 'y' => 'bar']);
$bulk->insert(['x' => 3, 'y' => 'bar']);
$manager->executeBulkWrite('db.collection', $bulk);

$command = new MongoDB\Driver\Command([
    'aggregate' => 'collection',
    'pipeline' => [
        ['$group' => ['_id' => '$y', 'sum' => ['$sum' => '$x']]],
    ],
    'cursor' => new stdClass,
]);
$cursor = $manager->executeCommand('db', $command);

/* Команда aggragete опционально может вернуть результаты в курсоре вместо
 * одиночного документа. В таком случае мы можем перебирать на курсоре для
 * непосредственного доступа к результатам. */
foreach ($cursor as $document) {
    var_dump($document);
}

?>
```

Результат виконання цього прикладу:

```
object(stdClass)#6 (2) {
  ["_id"]=>
  string(3) "bar"
  ["sum"]=>
  int(10)
}
object(stdClass)#7 (2) {
  ["_id"]=>
  string(3) "foo"
  ["sum"]=>
  int(2)
}
```

**Приклад #3 Обмеження часу виконання запиту**

Опція `"maxTimeMS"` класу [MongoDBDriverQuery](class.mongodb-driver-query.md) може використовуватись для обмеження часу виконання запиту. Зауважте, що цей термін застосовується на стороні сервера і не враховує затримки мережі. Дивіться [» Завершення виконання операцій](https://www.mongodb.com/docs/manual/tutorial/terminate-running-operations/#maxtimems) у посібнику MongoDB для отримання додаткової інформації.

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');

$command = new MongoDB\Driver\Command([
    'count' => 'collection',
    'query' => ['x' => ['$gt' => 1]],
    'maxTimeMS' => 1000,
]);

$cursor = $manager->executeCommand('db', $command);

var_dump($cursor->toArray()[0]);

?>
```

Якщо запит не завершиться через секунду після початку виконання на сервері, буде викинуто виняток [MongoDBDriverExceptionExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.md)

### Примітки

> **Зауваження**: Якщо використовується вторинний `readPreference`, відповідальність виконуючого коду гарантувати, що `command` може бути виконаний на вторинному вузлі. Перевірка не виконується драйвером.

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.md)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.md)
-   [MongoDBDriverManager::executeReadCommand()](mongodb-driver-manager.executereadcommand.md) - Виконує команду бази даних, яка читає
-   [MongoDBDriverManager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.md) - Виконує команду бази даних, яка читає та пише
-   [MongoDBDriverManager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.md) - Виконує команду бази даних, що пише
-   [MongoDBDriverServer::executeCommand()](mongodb-driver-server.executecommand.md) - Виконати команду бази даних на сервері
