Виконує запит до бази даних на сервері

-   [« MongoDB\\Driver\\Server::executeCommand](mongodb-driver-server.executecommand.html)
    
-   [MongoDB\\Driver\\Server::executeReadCommand »](mongodb-driver-server.executereadcommand.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
    
-   Виконує запит до бази даних на сервері
    

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

`query` [MongoDB\\Driver\\Query](class.mongodb-driver-query.html)

Запит на виконання.

`options`

**options**

| Опция                                                                            | Тип                                                                         | Описание |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|----------|
| readPreference                                                                   | [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html) |          |
| Перевага читання, що використовується для вибору сервера для виконання операції. |                                                                             |          |

| | session | [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)

Сесія зв'язування з операцією.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) інші помилки (наприклад, неприпустимі оператори запитів).

### список змін

| Версия             | Описание                                                                                                                                                                                     |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.4.0 | Третій параметр тепер є масивом `options`. Для зворотної сумісності цей параметр, як і раніше, прийматиме об'єкт [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html) |

### Дивіться також

-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
-   [MongoDB\\Driver\\Query](class.mongodb-driver-query.html)
-   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)
-   [MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.html) - Виконує запит до бази даних