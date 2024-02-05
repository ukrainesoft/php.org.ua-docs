---
navigation:
  - mongodb-driver-manager.executereadwritecommand.md: '« MongoDB\\Driver\\Manager::executeReadWriteCommand'
  - mongodb-driver-manager.getencryptedfieldsmap.md: 'MongoDB\\Driver\\Manager::getEncryptedFieldsMap »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::executeWriteCommand'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::executeWriteCommand

(mongodb >=1.4.0)

MongoDB\\Driver\\Manager::executeWriteCommand — Виконує команду бази даних, яка пише

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на основному сервері.

Цей метод застосовуватиме логіку, специфічну для команд, які пишуть (наприклад, [» drop](https://www.mongodb.com/docs/manual/reference/command/drop/)) та враховують версію сервера MongoDB. Опція `"writeConcern"` за умовчанням відповідатиме значенню з [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

> **Зауваження**: Метод не призначений для виконання [» insert](https://www.mongodb.com/docs/manual/reference/command/insert/) [» update](https://www.mongodb.com/docs/manual/reference/command/update/), или[» delete](https://www.mongodb.com/docs/manual/reference/command/delete/) команд. Користувачам рекомендується використовувати [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) для цих команд.

### Список параметрів

`db`(string)

Ім'я бази даних, у якій запускається команда.

`command` [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)) .

Команда для виконання.

`options`

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| session | [MongoDB\\Driver\\Session](class.mongodb-driver-session.md) |  |
| Сесія зв'язування з операцією. |  |  |

| | writeConcern |[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

**Увага**

При использовании`"session"` та наявності незавершених транзакцій, ви не можете вказати `"readConcern"`or`"writeConcern"` option. Це призведе до викидання винятків [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Натомість ви повинні встановити ці дві опції при створенні транзакції за допомогою [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.md)

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)

### Помилки

-   Викидається виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"`вказано з відповідною транзакцією у поєднанні з опцією`"readConcern"`или`"writeConcern"`
-   Викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"`вказано у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)інших помилок (наприклад, неправильна команда).

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.4.4 | Буде викинуто [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
-   [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md) \- Виконує команду бази даних
-   [MongoDB\\Driver\\Manager::executeReadCommand()](mongodb-driver-manager.executereadcommand.md) \- Виконує команду бази даних, яка читає
-   [MongoDB\\Driver\\Manager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.md) \- Виконує команду бази даних, яка читає та пише
-   [MongoDB\\Driver\\Server::executeWriteCommand()](mongodb-driver-server.executewritecommand.md) \- Виконує команду бази даних, що пише на сервері
