Виконує команду бази даних, яка читає та пише

-   [« MongoDBDriverManager::executeReadCommand](mongodb-driver-manager.executereadcommand.html)
    
-   [MongoDBDriverManager::executeWriteCommand »](mongodb-driver-manager.executewritecommand.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverManager](class.mongodb-driver-manager.html)
    
-   Виконує команду бази даних, яка читає та пише
    

# MongoDBDriverManager::executeReadWriteCommand

(mongodb >=1.4.0)

MongoDBDriverManager::executeReadWriteCommand — Виконує команду бази даних, яка читає та пише

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeReadWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на основному сервері.

Цей метод буде застосовувати логіку, специфічну для команд, які читають та пишуть (наприклад, [» aggregate](https://www.mongodb.com/docs/manual/reference/command/aggregate/)) та враховують версію сервера MongoDB. Параметри `"readConcern"` і `"writeConcern"` за замовчуванням відповідають відповідним значенням з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

### Список параметрів

`db` (string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDBDriverCommand](class.mongodb-driver-command.html)

Команда для виконання.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| readConcern | [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html) |  |
| Гарантія для застосування до операції. |  |  |

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | session | [MongoDBDriverSession](class.mongodb-driver-session.html)

Сесія зв'язування з операцією.

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
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) інших помилок (наприклад, неправильна команда).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) буде викинуто, якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.html)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.html)
-   [MongoDBDriverManager::executeCommand()](mongodb-driver-manager.executecommand.html) - Виконує команду бази даних
-   [MongoDBDriverManager::executeReadCommand()](mongodb-driver-manager.executereadcommand.html) - Виконує команду бази даних, яка читає
-   [MongoDBDriverManager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.html) - Виконує команду бази даних, що пише
-   [MongoDBDriverServer::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише на сервері