Вибрати сервер, що відповідає перевагам читання

-   [« MongoDB\\Driver\\Manager::removeSubscriber](mongodb-driver-manager.removesubscriber.html)
    
-   [MongoDB\\Driver\\Manager::startSession »](mongodb-driver-manager.startsession.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html)
    
-   Вибрати сервер, що відповідає перевагам читання
    

# MongoDBDriverManager::selectServer

(mongodb >=1.0.0)

MongoDBDriverManager::selectServer — Вибрати сервер, який відповідає перевагам читання

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::selectServer(?MongoDB\Driver\ReadPreference $readPreference = null): MongoDB\Driver\Server
```

Вибирає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), відповідний `readPreference`. Якщо параметр `readPreference` дорівнює **`null`** або опущено, за промовчанням буде обрано первинний сервер. Це можна використовувати для попереднього вибору сервера, щоб перевірити версію перед виконанням операції.

> **Зауваження**: На відміну від [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.html), цей метод ініціалізуватиме підключення до бази даних і при необхідності виконувати виявлення сервера. Детальніше дивіться . [» Спецификацию выбора сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst#single-threaded-server-selection)

### Список параметрів

`readPreference` [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)

Перевага читання використовується для вибору сервера. Якщо **`null`** або опущено, за промовчанням буде обрано первинний сервер.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html), Що відповідає перевагу читання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   При неможливості знайти сервер, що відповідає перевагу читання, викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.11.0 | Параметр `readPreference` тепер необов'язковий. Якщо вказано значення **`null`** або опущено, за промовчанням буде обрано первинний сервер. |

### Дивіться також

-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)
-   [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.html) - Повертає сервери, до яких підключено менеджера
-   [» Спецификация выбора сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst)