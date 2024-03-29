---
navigation:
  - mongodb-driver-manager.executequery.md: '« MongoDB\\Driver\\Manager::executeQuery'
  - mongodb-driver-manager.executereadwritecommand.md: 'MongoDB\\Driver\\Manager::executeReadWriteCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::executeReadCommand'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::executeReadCommand

(mongodb >=1.4.0)

MongoDB\\Driver\\Manager::executeReadCommand — Виконує команду бази даних, яка читає

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeReadCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
```

Вибирає сервер відповідно до опції `"readPreference"` та виконує команду на сервері. За замовчуванням буде використовуватися перевага читання з [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

Цей метод застосовуватиме логіку, специфічну для команд, які читають (наприклад, [» count](https://www.mongodb.com/docs/manual/reference/command/count/)) та враховують версію сервера MongoDB. Опція `"readConcern"` буде за умовчанням відповідати відповідному значенню з [URI підключення MongoDB](mongodb-driver-manager.construct.md#mongodb-driver-manager.construct-uri)

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
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)інших помилок (наприклад, неправильна команда).

### Дивіться також

-   [MongoDB\\Driver\\Command](class.mongodb-driver-command.md)
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
-   [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md) \- Виконує команду бази даних
-   [MongoDB\\Driver\\Manager::executeReadWriteCommand()](mongodb-driver-manager.executereadwritecommand.md) \- Виконує команду бази даних, яка читає та пише
-   [MongoDB\\Driver\\Manager::executeWriteCommand()](mongodb-driver-manager.executewritecommand.md) \- Виконує команду бази даних, що пише
-   [MongoDB\\Driver\\Server::executeReadCommand()](mongodb-driver-server.executereadcommand.md) \- Виконує команду бази даних, яка читає на сервері
