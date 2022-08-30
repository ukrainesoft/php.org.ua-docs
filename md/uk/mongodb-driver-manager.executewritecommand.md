Виконує команду бази даних, що пише

-   [« MongoDBDriverManager::executeReadWriteCommand](mongodb-driver-manager.executereadwritecommand.html)
    
-   [MongoDBDriverManager::getEncryptedFieldsMap »](mongodb-driver-manager.getencryptedfieldsmap.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverManager](class.mongodb-driver-manager.html)
    
-   Виконує команду бази даних, що пише
    

# MongoDBDriverManager::executeWriteCommand

(mongodb >=1.4.0)

MongoDBDriverManager::executeWriteCommand — Виконує команду бази даних, яка пише

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на основному сервері.

Цей метод застосовуватиме логіку, специфічну для команд, які пишуть (наприклад, [» drop](https://www.mongodb.com/docs/manual/reference/command/drop/)) та враховують версію сервера MongoDB. Опція `"writeConcern"` за умовчанням відповідатиме значенню з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

> **Зауваження**: Метод не призначений для виконання [» insert](https://www.mongodb.com/docs/manual/reference/command/insert/) [» update](https://www.mongodb.com/docs/manual/reference/command/update/), або [» delete](https://www.mongodb.com/docs/manual/reference/command/delete/) команд. Користувачам рекомендується використовувати [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html) для цих команд.

### Список параметрів

`db` (string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDBDriverCommand](class.mongodb-driver-command.html)

Команда для виконання.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| session | [MongoDBDriverSession](class.mongodb-driver-session.html) |  |
| Сесія зв'язування з операцією. |  |  |

| | writeConcern | [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html)

Гарантія запису для застосування до операції.

**Увага**

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.html)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverCursor](class.mongodb-driver-cursor.html)

### Помилки

-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   Викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) інших помилок (наприклад, неправильна команда).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | Буде викинуто [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.html)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.html)
-   [MongoDBDriverManager::executeCommand()](mongodb-driver-manager.executecommand.html) - Виконує команду бази даних
-   [MongoDBDriverManager::executeReadCommand()](mongodb-driver-manager.executereadcommand.html) - Виконує команду бази даних, яка читає
-   [MongoDBDriverManager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише
-   [MongoDBDriverServer::executeWriteCommand()](mongodb-driver-server.executewritecommand.html) - Виконує команду бази даних, що пише на сервері