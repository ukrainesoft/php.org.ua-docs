---
navigation:
  - mongodb-driver-server.construct.md: '« MongoDBDriverServer::construct'
  - mongodb-driver-server.executecommand.md: 'MongoDBDriverServer::executeCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::executeBulkWrite'
---
# MongoDBDriverServer::executeBulkWrite

(mongodb >=1.0.0)

MongoDBDriverServer::executeBulkWrite — Виконати одну або кілька операцій запису на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeBulkWrite(string $namespace, MongoDB\Driver\BulkWrite $bulk, array|MongoDB\Driver\WriteConcern|null $options = null): MongoDB\Driver\WriteResult
```

Виконує одну або кілька операцій запису на сервері.

Об'єкт [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md) може бути створений з однією або декількома операціями запису різного типу (наприклад, оновлення, видалення та вставки). Драйвер спробує надіслати операції одного типу на сервер у вигляді якнайменшої кількості запитів для скорочення звернень до сервера.

### Список параметрів

`namespace` (string)

Повністю певне ім'я (тобто . `"databaseName.collectionName"`

`bulk` [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md)

Записи для виконання.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| session | [MongoDBDriverSession](class.mongodb-driver-session.md) |  |
| Сесія зв'язування з операцією. |  |  |

| | writeConcern | [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.md)

### Помилки

-   За відсутності операцій запису в `bulk` викидає [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Якщо `bulk` вже був виконаний, викидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Об'єкти [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md) не можуть бути виконані кілька разів.
-   Викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   При помилці запису кидає виняток [MongoDBDriverExceptionBulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md)
-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   У разі інших помилок викидає [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.4 | Якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису, викидається виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. Для зворотної сумісності цей параметр все одно прийме об'єкт [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) |
| PECL mongodb 1.3.0 | Якщо `bulk` не містить операцій запису, викидається [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Раніше викидалося [MongoDBDriverExceptionBulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md) |

### Примітки

> **Зауваження**: Відповідальність коду, що викликає, полягає в тому, що сервер в змозі виконувати операцію запису. Наприклад, виконання операції запису на вторинному вузлі (за винятком "локальної" бази даних) завершиться невдачею.

### Дивіться також

-   [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md)
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.md)
-   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)
-   [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) - Виконує одну або кілька операцій запису
