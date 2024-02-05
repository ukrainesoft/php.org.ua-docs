---
navigation:
  - mongodb-driver-server.construct.md: '« MongoDB\\Driver\\Server::\_\_construct'
  - mongodb-driver-server.executecommand.md: 'MongoDB\\Driver\\Server::executeCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::executeBulkWrite'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::executeBulkWrite

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::executeBulkWrite — Виконати одну або кілька операцій запису на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeBulkWrite(string $namespace, MongoDB\Driver\BulkWrite $bulk, array|MongoDB\Driver\WriteConcern|null $options = null): MongoDB\Driver\WriteResult
```

Виконує одну або кілька операцій запису на сервері.

Об'єкт [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md) може бути створений з однією або декількома операціями запису різного типу (наприклад, оновлення, видалення та вставки). Драйвер спробує надіслати операції одного типу на сервер у вигляді якнайменшої кількості запитів для скорочення звернень до сервера.

### Список параметрів

`namespace`(string)

Повністю певне ім'я (тобто . `"databaseName.collectionName"`

`bulk` [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)) .

Записи для виконання.

`options`

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| session | [MongoDB\\Driver\\Session](class.mongodb-driver-session.md) |  |
| Сесія зв'язування з операцією. |  |  |

| | writeConcern |[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)

### Помилки

-   За відсутності операцій запису в`bulk` викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Якщо `bulk`вже був виконаний, викидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Об'єкти[MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)не можуть бути виконані кілька разів.
-   Викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"`вказано у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   При помилці запису кидає виняток[MongoDB\\Driver\\Exception\\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md)
-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   У разі інших помилок викидає[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.4.4 | Якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису, викидається виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. . Для зворотної сумісності цей параметр все одно прийме об'єкт [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md) |
| PECL mongodb 1.3.0 | Якщо `bulk` не містить операцій запису, викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). . Раніше викидалося [MongoDB\\Driver\\Exception\\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md) |

### Примітки

> **Зауваження**: Відповідальність коду, що викликає, полягає в тому, що сервер в змозі виконувати операцію запису. Наприклад, виконання операції запису на вторинному вузлі (за винятком «локальної» бази даних) завершиться невдачею.

### Дивіться також

-   [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)
-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) \- Виконує одну або кілька операцій запису
