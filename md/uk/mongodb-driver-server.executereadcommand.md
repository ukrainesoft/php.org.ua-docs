---
navigation:
  - mongodb-driver-server.executequery.md: '« MongoDB\\Driver\\Server::executeQuery'
  - mongodb-driver-server.executereadwritecommand.md: 'MongoDB\\Driver\\Server::executeReadWriteCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::executeReadCommand'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::executeReadCommand

(mongodb >=1.4.0)

MongoDB\\Driver\\Server::executeReadCommand — Виконує команду бази даних, яка читає на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeReadCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на цьому сервері.

Цей метод застосовуватиме логіку, специфічну для команд, які читають (наприклад, [» count](https://www.mongodb.com/docs/manual/reference/command/count/)) та враховують версію сервера MongoDB. Опція `"readConcern"` буде за умовчанням відповідати відповідному значенню з [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

> **Зауваження**: Опция`"readPreference"` не контролює сервер, якого драйвер виконує операцію; вона завжди виконуватиметься на цьому об'єкті сервера. Натомість, він може бути використаний при виконанні операції на другому вузлі (з набору реплік, не автономний) або на вузлі mongos для забезпечення того, що драйвер встановлює дротовий протокол відповідним чином або додає перевагу читання до операції відповідно.

### Список параметрів

`db`(string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)) .

Команда для виконання.

`options`

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| readConcern | [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md) |  |
| Гарантія для застосування до операції. |  |  |

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference |[MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | session |[MongoDB\\Driver\\Session](class.mongodb-driver-session.md)

Сесія зв'язування з операцією.

**Увага**

При использовании`"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"`or`"writeConcern"` option. Це призведе до викидання винятків [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.md)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)

### Помилки

-   Викидається виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"`вказано з відповідною транзакцією у поєднанні з опцією`"readConcern"`или`"writeConcern"`
-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)інші помилки (наприклад, неправильна команда ).

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
-   [MongoDB\\Driver\\Server::executeCommand()](mongodb-driver-server.executecommand.md) \- Виконати команду бази даних на сервері
-   [MongoDB\\Driver\\Server::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.md) \- Виконує команду бази даних, яка читає та пише на сервері
-   [MongoDB\\Driver\\Server::executeWriteCommand()](mongodb-driver-server.executewritecommand.md) \- Виконує команду бази даних, що пише на сервері
-   [MongoDB\\Driver\\Manager::executeReadCommand()](mongodb-driver-manager.executereadcommand.md) \- Виконує команду бази даних, яка читає
