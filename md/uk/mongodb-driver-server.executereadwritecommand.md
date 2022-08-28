Виконує команду бази даних, яка читає та пише на сервері

-   [« MongoDB\\Driver\\Server::executeReadCommand](mongodb-driver-server.executereadcommand.html)
    
-   [MongoDB\\Driver\\Server::executeWriteCommand »](mongodb-driver-server.executewritecommand.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Виконує команду бази даних, яка читає та пише на сервері
    

# MongoDBDriverServer::executeReadWriteCommand

(mongodb >=1.4.0)

MongoDBDriverServer::executeReadWriteCommand — Виконує команду бази даних, яка читає та пише на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeReadWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на сервері.

Цей метод буде застосовувати логіку, специфічну для команд, які читають та пишуть (наприклад, [» aggregate](https://www.mongodb.com/docs/manual/reference/command/aggregate/)) та враховують версію сервера MongoDB. Параметри `"readConcern"` і `"writeConcern"` за замовчуванням відповідають відповідним значенням з [URI подключения MongoDB](mongodb-driver-manager.construct.html#mongodb-driver-manager.construct-uri)

### Список параметрів

`db` (string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)

Команда для виконання.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| readConcern | [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html) |  |
| Гарантія для застосування до операції. |  |  |

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | session | [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)

Сесія зв'язування з операцією.

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
-   Видає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) інші помилки (наприклад, неправильна команда).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) буде викинуто, якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Примітки

> **Зауваження**: Відповідальність коду, що викликає, полягає в тому, що сервер в змозі виконувати операцію запису. Наприклад, виконання операції запису на вторинному вузлі (за винятком "локальної" бази даних) завершиться невдачею.

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
-   [MongoDB\\Driver\\Server::executeCommand()](mongodb-driver-server.executecommand.html) - Виконати команду бази даних на сервері
-   [MongoDB\\Driver\\Server::executeReadCommand()](mongodb-driver-server.executereadcommand.html) - Виконує команду бази даних, яка читає на сервері
-   [MongoDB\\Driver\\Server::executeWriteCommand()](mongodb-driver-server.executewritecommand.html) - Виконує команду бази даних, що пише на сервері
-   [MongoDB\\Driver\\Manager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.html) - Виконує команду бази даних, яка читає та пише