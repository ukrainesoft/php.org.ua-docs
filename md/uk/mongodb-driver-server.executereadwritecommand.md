---
navigation:
  - mongodb-driver-server.executereadcommand.md: '« MongoDBDriverServer::executeReadCommand'
  - mongodb-driver-server.executewritecommand.md: 'MongoDBDriverServer::executeWriteCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::executeReadWriteCommand'
---
# MongoDBDriverServer::executeReadWriteCommand

(mongodb >=1.4.0)

MongoDBDriverServer::executeReadWriteCommand — Виконує команду бази даних, яка читає та пише на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeReadWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на сервері.

Цей метод буде застосовувати логіку, специфічну для команд, які читають та пишуть (наприклад, [» aggregate](https://www.mongodb.com/docs/manual/reference/command/aggregate/)) та враховують версію сервера MongoDB. Параметри `"readConcern"` і `"writeConcern"` за замовчуванням відповідають відповідним значенням з [URI подключения MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

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

| | session | [MongoDBDriverSession](class.mongodb-driver-session.md)

Сесія зв'язування з операцією.

| | writeConcern | [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

**Увага**

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.md)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverCursor](class.mongodb-driver-cursor.md)

### Помилки

-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md) інші помилки (наприклад, неправильна команда).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) буде викинуто, якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Примітки

> **Зауваження**: Відповідальність коду, що викликає, полягає в тому, що сервер в змозі виконувати операцію запису. Наприклад, виконання операції запису на вторинному вузлі (за винятком "локальної" бази даних) завершиться невдачею.

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.md)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.md)
-   [MongoDBDriverServer::executeCommand()](mongodb-driver-server.executecommand.md) - Виконати команду бази даних на сервері
-   [MongoDBDriverServer::executeReadCommand()](mongodb-driver-server.executereadcommand.md) - Виконує команду бази даних, яка читає на сервері
-   [MongoDBDriverServer::executeWriteCommand()](mongodb-driver-server.executewritecommand.md) - Виконує команду бази даних, що пише на сервері
-   [MongoDBDriverManager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.md) - Виконує команду бази даних, яка читає та пише
