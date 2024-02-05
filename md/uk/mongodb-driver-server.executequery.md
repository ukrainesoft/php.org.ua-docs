---
navigation:
  - mongodb-driver-server.executecommand.md: '« MongoDB\\Driver\\Server::executeCommand'
  - mongodb-driver-server.executereadcommand.md: 'MongoDB\\Driver\\Server::executeReadCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::executeQuery'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::executeQuery

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::executeQuery — Виконує запит до бази даних на сервері

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::executeQuery(string $namespace, MongoDB\Driver\Query $query, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
```

Виконує запит на сервері.

> **Зауваження**: Опция`"readPreference"` не керує сервером, якому драйвер виконує операцію; він завжди виконуватиметься на цьому об'єкті сервера. Натомість його можна використовувати при видачі операції на вторинному сервері (зі з'єднання з реплікою, а не автономному) або вузол mongos, щоб гарантувати, що драйвер відповідно встановлює дротовий протокол або додає переваги читання до операції відповідно.

### Список параметрів

`namespace`(string)

Повністю певне ім'я (тобто . `"databaseName.collectionName"`

`query` [MongoDB\\Driver\\Query](class.mongodb-driver-query.md)) .

Запит на виконання.

`options`

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| readPreference | [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md) |  |
| Перевага читання, що використовується для вибору сервера для виконання операції. |  |  |

| | session |[MongoDB\\Driver\\Session](class.mongodb-driver-session.md)

Сесія зв'язування з операцією.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)інші помилки (наприклад, неприпустимі оператори запитів).

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. . Для зворотної сумісності цей параметр, як і раніше, прийматиме об'єкт [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md) |

### Дивіться також

-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)
-   [MongoDB\\Driver\\Query](class.mongodb-driver-query.md)
-   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)
-   [MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.md) \- Виконує запит до бази даних
