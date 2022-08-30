Виконує команду бази даних, яка читає на сервері

-   [« MongoDBDriverServer::executeQuery](mongodb-driver-server.executequery.html)
    
-   [MongoDBDriverServer::executeReadWriteCommand »](mongodb-driver-server.executereadwritecommand.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverServer](class.mongodb-driver-server.html)
    
-   Виконує команду бази даних, яка читає на сервері
    

# MongoDBDriverServer::executeReadCommand

(mongodb >=1.4.0)

MongoDBDriverServer::executeReadCommand — Виконує команду бази даних, яка читає на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeReadCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на цьому сервері.

Цей метод застосовуватиме логіку, специфічну для команд, які читають (наприклад, [» count](https://www.mongodb.com/docs/manual/reference/command/count/)) та враховують версію сервера MongoDB. Опція `"readConcern"` буде за умовчанням відповідати відповідному значенню з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

> **Зауваження**: Опція `"readPreference"` не контролює сервер, якого драйвер виконує операцію; вона завжди виконуватиметься на цьому об'єкті сервера. Натомість, він може бути використаний при виконанні операції на другому вузлі (з набору реплік, не автономний) або на вузлі mongos для забезпечення того, що драйвер встановлює дротовий протокол відповідним чином або додає перевагу читання до операції відповідно.

### Список параметрів

`db` (string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDBDriverCommand](class.mongodb-driver-command.html)

Команда для виконання.

`options`

**options**

| Опция                                  | Тип                                                               | Описание |
|----------------------------------------|-------------------------------------------------------------------|----------|
| readConcern                            | [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html) |          |
| Гарантія для застосування до операції. |                                                                   |          |

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
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) інші помилки (наприклад, неправильна команда ).

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.html)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.html)
-   [MongoDBDriverServer::executeCommand()](mongodb-driver-server.executecommand.html) - Виконати команду бази даних на сервері
-   [MongoDBDriverServer::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDBDriverServer::executeWriteCommand()](mongodb-driver-server.executewritecommand.html) - Виконує команду бази даних, що пише на сервері
-   [MongoDBDriverManager::executeReadCommand()](mongodb-driver-manager.executereadcommand.html) - Виконує команду бази даних, яка читає