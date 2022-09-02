---
navigation:
  - mongodb-driver-server.executebulkwrite.md: '« MongoDBDriverServer::executeBulkWrite'
  - mongodb-driver-server.executequery.md: 'MongoDBDriverServer::executeQuery »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::executeCommand'
---
# MongoDBDriverServer::executeCommand

(mongodb >=1.0.0)

MongoDBDriverServer::executeCommand — Виконати команду бази даних на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeCommand(string $db, MongoDB\Driver\Command $command, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
```

Виконує команду на сервері.

Цей метод не застосовує особливої ​​логіки до команди. Хоча цей метод приймає `"readConcern"` і `"writeConcern"`, які будуть включені в документи коанди, ці опції не будуть відповідати значенням за замовчуванням [MongoDB URI соединения](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri) , і не враховуватиметься версія сервера MongoDB. Тому користувачам рекомендується використовувати конкретні методи команди читання та/або запису, якщо це можливо.

> **Зауваження**: Опція `"readPreference"` не контролює сервер, якого драйвер виконує операцію; вона завжди виконуватиметься на цьому об'єкті сервера. Замість цього він може бути використаний при виконанні операції на другому вузлі (з набору реплік, не автономний) або на вузлі mongos для забезпечення того, що драйвер встановлює дротовий протокол відповідним чином або додає перевагу читання до операції відповідно.

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

При використанні `"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"` ор `"writeConcern"` option. Це призведе до викидання винятків [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.md)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverCursor](class.mongodb-driver-cursor.md)

### Помилки

-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується з відповідною транзакцією у поєднанні з опцією `"readConcern"` або `"writeConcern"`
-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md) у разі інших помилок (наприклад, неправильна команда, видача команди записи на вторинний пристрій).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | Якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису, викидається виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. Для зворотної сумісності цей параметр все одно прийме об'єкт [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) |

### Примітки

> **Зауваження**: Відповідальність коду, що викликає, полягає в тому, що сервер в змозі виконувати операцію запису. Наприклад, виконання операції запису на вторинному вузлі (за винятком "локальної" бази даних) завершиться невдачею.

### Дивіться також

-   [MongoDBDriverCommand](class.mongodb-driver-command.md)
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.md)
-   [MongoDBDriverServer::executeReadCommand()](mongodb-driver-server.executereadcommand.md) - Виконує команду бази даних, яка читає на сервері
-   [MongoDBDriverServer::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.md) - Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDBDriverServer::executeWriteCommand()](mongodb-driver-server.executewritecommand.md) - Виконує команду бази даних, що пише на сервері
-   [MongoDBDriverManager::executeCommand()](mongodb-driver-manager.executecommand.md) - Виконує команду бази даних
