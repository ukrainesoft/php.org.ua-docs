---
navigation:
  - mongodb-driver-manager.executereadcommand.md: '« MongoDB\\Driver\\Manager::executeReadCommand'
  - mongodb-driver-manager.executewritecommand.md: 'MongoDB\\Driver\\Manager::executeWriteCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::executeReadWriteCommand'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::executeReadWriteCommand

(mongodb >=1.4.0)

MongoDB\\Driver\\Manager::executeReadWriteCommand — Виконує команду бази даних, яка читає та пише

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeReadWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Виконує команду на основному сервері.

Цей метод буде застосовувати логіку, специфічну для команд, які читають та пишуть (наприклад, [» aggregate](https://www.mongodb.com/docs/manual/reference/command/aggregate/)) та враховують версію сервера MongoDB. Параметри `"readConcern"`и`"writeConcern"`по умолчанию соответствуют соответствующим значениям из[URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

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

| | session |[MongoDB\\Driver\\Session](class.mongodb-driver-session.md)

Сесія зв'язування з операцією.

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
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)інших помилок (наприклад, неправильна команда).

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.4.4 | [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) буде викинуто, якщо опція `"session"` використовується у поєднанні з непідтвердженим записом. |

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
-   [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md) \- Виконує команду бази даних
-   [MongoDB\\Driver\\Manager::executeReadCommand()](mongodb-driver-manager.executereadcommand.md) \- Виконує команду бази даних, яка читає
-   [MongoDB\\Driver\\Manager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.md) \- Виконує команду бази даних, що пише
-   [MongoDB\\Driver\\Server::executeReadWriteCommand()](mongodb-driver-server.executereadwritecommand.md) \- Виконує команду бази даних, яка читає та пише на сервері
