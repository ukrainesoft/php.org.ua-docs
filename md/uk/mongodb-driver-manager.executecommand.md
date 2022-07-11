- [« MongoDB\Driver\Manager::executeBulkWrite](mongodb-driver-manager.executebulkwrite.md)
- [MongoDB\Driver\Manager::executeQuery »](mongodb-driver-manager.executequery.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\Manager](class.mongodb-driver-manager.md)
- Виконує команду бази даних

# MongoDB\Driver\Manager::executeCommand

(mongodb \>=1.0.0)

MongoDB\Driver\Manager::executeCommand — Виконує команду бази даних

### Опис

final public **MongoDB\Driver\Manager::executeCommand**(string `$db`,
[MongoDB\Driver\Command](class.mongodb-driver-command.md) `$command`,
array `$options` = array()):
[MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)

Вибирає сервер відповідно до опції ``readPreference'` і виконує
запит на цьому сервері. За замовчуванням використовуватиметься перевага
читання з URI [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri).

Цей метод не застосовує особливої логіки до команди. Хоча цей метод
приймає ``readConcern'' та ``writeConcern'', які будуть включені в
документи коанди, ці опції не відповідатимуть значенням по
замовчуванням з [MongoDB URI з'єднання](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)
, і не враховуватиметься версія сервера MongoDB. Тому користувачам
рекомендується використовувати конкретні методи команди читання та/або запису
якщо це можливо.

### Список параметрів

`db` (string)
Назва бази даних, в якій запускається команда.

`command` ([MongoDB\Driver\Command](class.mongodb-driver-command.md))
Команда для виконання.

`options`
[TABLE]

**options**

**Увага**
При використанні `session` та наявності незавершених транзакцій, ви не
можете вказати ``readConcern'' або 'writeConcern' option. Це приведе
до викидання виключення [MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).
Натомість ви повинні встановити ці дві опції при створенні транзакції
за допомогою
[MongoDB\Driver\Session::startTransaction()](mongodb-driver-session.starttransaction.md).

### Значення, що повертаються

У разі успішного виконання повертає
[MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md).

### Помилки

- Викидається
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md),
якщо опція ``session'` використовується з відповідною транзакцією в
поєднанні з опцією `readConcern` або `writeConcern`.
- Викидається
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md),
якщо опція ``session'` використовується в поєднанні з непідтвердженим
гарантією запису.
- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).
- При невдалому з'єднанні з сервером (крім помилок автентифікації),
кидає виняток
[MongoDB\Driver\Exception\ConnectionException](class.mongodb-driver-exception-connectionexception.md).
- За невдалої аутентифікації кидає виняток
[MongoDB\Driver\Exception\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md).
- При виникненні інших помилок (наприклад, неправильна команда),
викидає виняток
[MongoDB\Driver\Exception\RuntimeException](class.mongodb-driver-exception-runtimeexception.md).

### Список змін

| Версія             | Опис                                                                                                                                                                                                                       |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.4.4 | Якщо опція "session" використовується в поєднанні з непідтвердженою гарантією запису, викидається виняток [MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом options. Для зворотної сумісності цей параметр все одно прийме об'єкт [MongoDB\Driver\ReadPreference](class.mongodb-driver-readpreference.md).                                             |

### Приклади

**Приклад #1 Приклад використання
**MongoDB\Driver\Manager::executeCommand()** з командою, що повертає
одиночний документ**

` <?php$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');$command = new MongoDB\Driver\Command(['ping' => 1]);try {     $cursor $manager->executeCommand('admin', $command);} catch(MongoDB\Driver\Exception $e) {   echo $e->getMessage(), "
";    exit;}/* Команда ping повертає одинаковий результат, тому ми маємо отримати доступ к * першому результату в курсор. */$response ==;

Результат виконання цього прикладу:

array(1) {
["ok"]=>
float(1)
}

**Приклад #2 Приклад використання
**MongoDB\Driver\Manager::executeCommand()** з командою, що повертає
курсор**

` <?php$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['x' => 1, ' y' => 'foo']);$bulk->insert(['x' => 2, 'y' => 'bar']);$bulk->insert(['x' => 3, ' y' => 'bar']);$manager->executeBulkWrite('db.collection', $bulk);$command = new MongoDB\Driver\Command([   'aggregate' => 'collection', | > [        ['$group' => ['_id' => '$y', 'sum' => ['$sum' => '$x']]],    ],      ]);$cursor = $manager->executeCommand('db', $command);/* Команда aggragete опціонально може повернути результати в курсорі замість * одинакового документу. У такому випадку ми можемо перебирати на курсорі для безпосереднього доступу до результатів. */foreach ($cursor as $document) {    var_dump($document);}?> `

Результат виконання цього прикладу:

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

**Приклад #3 Обмеження часу виконання запиту**

Опція ``maxTimeMS'` класу
[MongoDB\Driver\Query](class.mongodb-driver-query.md) може
використовуватись для обмеження часу виконання запиту. Зверніть
увагу, що цей термін застосовується на стороні сервера та не враховує
затримки мережі. Дивіться [» Завершення виконання операцій](https://www.mongodb.com/docs/manual/tutorial/terminate-running-operations/#maxtimems)
у посібнику MongoDB для отримання додаткової інформації.

` <?php$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');$command = new MongoDB\Driver\Command([   'count' => 'collection', > | ['x' => ['$gt' => 1]],   'maxTimeMS' => 1000,]);$cursor = $manager->executeCommand('db', $command);var_dump($cursor-> toArray()[0]);?> `

Якщо запит не завершиться через секунду після початку виконання на
сервері, буде викинуто виняток [MongoDB\Driver\Exception\ExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.md).

### Примітки

> **Примітка**: Якщо використовується вторинний `readPreference`,
> відповідальність виконуючого коду гарантувати, що `command` може
> бути виконаний на вторинному вузлі. Перевірка не виконується драйвером.

### Дивіться також

- [MongoDB\Driver\Command](class.mongodb-driver-command.md)
- [MongoDB\Driver\Cursor](class.mongodb-driver-cursor.md)
- [MongoDB\Driver\Manager::executeReadCommand()](mongodb-driver-manager.executereadcommand.md) -
Виконує команду бази даних, яка читає
- [MongoDB\Driver\Manager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.md) -
Виконує команду бази даних, яка читає та пише
- [MongoDB\Driver\Manager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.md) -
Виконує команду бази даних, що пише
- [MongoDB\Driver\Server::executeCommand()](mongodb-driver-server.executecommand.md) -
Виконати команду бази даних на сервері
