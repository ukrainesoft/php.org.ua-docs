Виконує команду бази даних, що пише на сервері

-   [« MongoDB\\Driver\\Server::executeReadWriteCommand](mongodb-driver-server.executereadwritecommand.html)
    
-   [MongoDB\\Driver\\Server::getHost »](mongodb-driver-server.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Виконує команду бази даних, що пише на сервері
    

# MongoDBDriverServer::executeWriteCommand

(mongodb >=1.4.0)

MongoDBDriverServer::executeWriteCommand — Виконує команду бази даних, яка пише на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на цьому сервері.

Цей метод застосовуватиме логіку, специфічну для команд, які пишуть (наприклад, [» drop](https://www.mongodb.com/docs/manual/reference/command/drop/)) та враховують версію сервера MongoDB. Опція `"writeConcern"` за умовчанням відповідатиме відповідному значенню з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

> **Зауваження**: Метод не призначений для виконання [» insert](https://www.mongodb.com/docs/manual/reference/command/insert/) [» update](https://www.mongodb.com/docs/manual/reference/command/update/), або [» delete](https://www.mongodb.com/docs/manual/reference/command/delete/) команд. Користувачам рекомендується використовувати [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html) для цих команд.

### Список параметрів

`db` (string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)

Команда для виконання.

`options`

**options**

| Опция                          | Тип                                                           | Описание |
|--------------------------------|---------------------------------------------------------------|----------|
| session                        | [MongoDB\\Driver\\Session](class.mongodb-driver-session.html) |          |
| Сесія зв'язування з операцією. |                                                               |          |

| | writeConcern | [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)

Гарантія запису для застосування до операції.

**Увага**

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.html)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)

### Помилки

-   Викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   Викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) інші помилки (наприклад, неправильна команда).

### список змін

| Версия             | Описание                                                                                                                                                                                                         |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.4.4 | Буде викинуто [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Примітки

> **Зауваження**: Відповідальність коду, що викликає, полягає в тому, що сервер в змозі виконувати операцію запису. Наприклад, виконання операції запису на вторинному вузлі (за винятком "локальної" бази даних) завершиться невдачею.

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
-   [MongoDB\\Driver\\Server::executeCommand()](mongodb-driver-server.executecommand.html) - Виконати команду бази даних на сервері
-   [MongoDB\\Driver\\Server::executeReadCommand()](mongodb-driver-server.executereadcommand.html) - Виконує команду бази даних, яка читає на сервері
-   [MongoDB\\Driver\\Server::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDB\\Driver\\Manager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.html) - Виконує команду бази даних, що пише