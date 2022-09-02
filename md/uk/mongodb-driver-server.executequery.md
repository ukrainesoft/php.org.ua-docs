---
navigation:
  - mongodb-driver-server.executecommand.md: '« MongoDBDriverServer::executeCommand'
  - mongodb-driver-server.executereadcommand.md: 'MongoDBDriverServer::executeReadCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::executeQuery'
---
# MongoDBDriverServer::executeQuery

(mongodb >=1.0.0)

MongoDBDriverServer::executeQuery — Виконує запит до бази даних на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeQuery(string $namespace, MongoDB\Driver\Query $query, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
```

Виконує запит на сервері.

> **Зауваження**: Опція `"readPreference"` не керує сервером, якому драйвер виконує операцію; він завжди виконуватиметься на цьому об'єкті сервера. Натомість його можна використовувати при видачі операції на вторинному сервері (зі з'єднання з реплікою, а не автономному) або вузол mongos, щоб гарантувати, що драйвер відповідно встановлює дротовий протокол або додає переваги читання до операції відповідно.

### Список параметрів

`namespace` (string)

Повністю певне ім'я (тобто . `"databaseName.collectionName"`

`query` [MongoDBDriverQuery](class.mongodb-driver-query.md)

Запит на виконання.

`options`

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| readPreference | [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) |  |
| Перевага читання, що використовується для вибору сервера для виконання операції. |  |  |

| | session | [MongoDBDriverSession](class.mongodb-driver-session.md)

Сесія зв'язування з операцією.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDBDriverCursor](class.mongodb-driver-cursor.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md) інші помилки (наприклад, неприпустимі оператори запитів).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. Для зворотної сумісності цей параметр, як і раніше, прийматиме об'єкт [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md) |

### Дивіться також

-   [MongoDBDriverCursor](class.mongodb-driver-cursor.md)
-   [MongoDBDriverQuery](class.mongodb-driver-query.md)
-   [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md)
-   [MongoDBDriverManager::executeQuery()](mongodb-driver-manager.executequery.md) - Виконує запит до бази даних
