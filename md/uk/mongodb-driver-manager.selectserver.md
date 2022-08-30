Вибрати сервер, що відповідає перевагам читання

-   [« MongoDBDriverManager::removeSubscriber](mongodb-driver-manager.removesubscriber.html)
    
-   [MongoDBDriverManager::startSession »](mongodb-driver-manager.startsession.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverManager](class.mongodb-driver-manager.html)
    
-   Вибрати сервер, що відповідає перевагам читання
    

# MongoDBDriverManager::selectServer

(mongodb >=1.0.0)

MongoDBDriverManager::selectServer — Вибрати сервер, який відповідає перевагам читання

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::selectServer(?MongoDB\Driver\ReadPreference $readPreference = null): MongoDB\Driver\Server
```

Вибирає [MongoDBDriverServer](class.mongodb-driver-server.html), відповідний `readPreference`. Якщо параметр `readPreference` дорівнює **`null`** або опущено, за промовчанням буде обрано первинний сервер. Це можна використовувати для попереднього вибору сервера, щоб перевірити версію перед виконанням операції.

> **Зауваження**: На відміну від [MongoDBDriverManager::getServers()](mongodb-driver-manager.getservers.html), цей метод ініціалізуватиме підключення до бази даних і при необхідності виконувати виявлення сервера. Детальніше дивіться . [» Специфікацію вибору сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst#single-threaded-server-selection)

### Список параметрів

`readPreference` [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)

Перевага читання використовується для вибору сервера. Якщо **`null`** або опущено, за промовчанням буде обрано первинний сервер.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html), Що відповідає перевагу читання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   При неможливості знайти сервер, що відповідає перевагу читання, викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html)

### список змін

| Версия              | Описание                                                                                                                                    |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.11.0 | Параметр `readPreference` тепер необов'язковий. Якщо вказано значення **`null`** або опущено, за промовчанням буде обрано первинний сервер. |

### Дивіться також

-   [MongoDBDriverServer](class.mongodb-driver-server.html)
-   [MongoDBDriverManager::getServers()](mongodb-driver-manager.getservers.html) - Повертає сервери, до яких підключено менеджера
-   [» Специфікація вибору сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst)