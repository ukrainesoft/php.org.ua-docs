Виконує команду бази даних, яка читає

-   [« MongoDBDriverManager::executeQuery](mongodb-driver-manager.executequery.html)
    
-   [MongoDBDriverManager::executeReadWriteCommand »](mongodb-driver-manager.executereadwritecommand.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverManager](class.mongodb-driver-manager.html)
    
-   Виконує команду бази даних, яка читає
    

# MongoDBDriverManager::executeReadCommand

(mongodb >=1.4.0)

MongoDBDriverManager::executeReadCommand — Виконує команду бази даних, яка читає

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeReadCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Вибирає сервер відповідно до опції `"readPreference"` та виконує команду на сервері. За замовчуванням буде використовуватися перевага читання з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

Цей метод застосовуватиме логіку, специфічну для команд, які читають (наприклад, [» count](https://www.mongodb.com/docs/manual/reference/command/count/)) та враховують версію сервера MongoDB. Опція `"readConcern"` буде за умовчанням відповідати відповідному значенню з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

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

| | readPreference | [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | session | [MongoDBDriverSession](class.mongodb-driver-session.html)

Сесія зв'язування з операцією.

**Увага**

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.html)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverCursor](class.mongodb-driver-cursor.html)

### Помилки

-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) інших помилок (наприклад, неправильна команда).

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.html)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.html)
-   [MongoDBDriverManager::executeCommand()](mongodb-driver-manager.executecommand.html) - Виконує команду бази даних
-   [MongoDBDriverManager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише
-   [MongoDBDriverManager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.html) - Виконує команду бази даних, що пише
-   [MongoDBDriverServer::executeReadCommand()](mongodb-driver-server.executereadcommand.html) - Виконує команду бази даних, яка читає на сервері