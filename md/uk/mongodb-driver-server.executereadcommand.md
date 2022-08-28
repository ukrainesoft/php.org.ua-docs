Виконує команду бази даних, яка читає на сервері

-   [« MongoDB\\Driver\\Server::executeQuery](mongodb-driver-server.executequery.html)
    
-   [MongoDB\\Driver\\Server::executeReadWriteCommand »](mongodb-driver-server.executereadwritecommand.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
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

`command` [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)

Команда для виконання.

`options`

**options**

| Опция                                  | Тип                                                                   | Описание |
|----------------------------------------|-----------------------------------------------------------------------|----------|
| readConcern                            | [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html) |          |
| Гарантія для застосування до операції. |                                                                       |          |

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference | [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | session | [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)

Сесія зв'язування з операцією.

**Увага**

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.html)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)

### Помилки

-   Викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) інші помилки (наприклад, неправильна команда ).

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
-   [MongoDB\\Driver\\Server::executeCommand()](mongodb-driver-server.executecommand.html) - Виконати команду бази даних на сервері
-   [MongoDB\\Driver\\Server::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDB\\Driver\\Server::executeWriteCommand()](mongodb-driver-server.executewritecommand.html) - Виконує команду бази даних, що пише на сервері
-   [MongoDB\\Driver\\Manager::executeReadCommand()](mongodb-driver-manager.executereadcommand.html) - Виконує команду бази даних, яка читає