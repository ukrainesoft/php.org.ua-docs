---
navigation:
  - mongodb-driver-manager.removesubscriber.md: '« MongoDB\\Driver\\Manager::removeSubscriber'
  - mongodb-driver-manager.startsession.md: 'MongoDB\\Driver\\Manager::startSession »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::selectServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::selectServer

(mongodb >=1.0.0)

MongoDB\\Driver\\Manager::selectServer — Вибрати сервер, який відповідає перевагам читання

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::selectServer(?MongoDB\Driver\ReadPreference $readPreference = null): MongoDB\Driver\Server
```

Вибирає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md), соответствующий`readPreference`. Якщо параметр `readPreference`равен\*\*`null`\*\* або опущено, за промовчанням буде обрано первинний сервер. Це можна використовувати для попереднього вибору сервера, щоб перевірити версію перед виконанням операції.

> **Зауваження**: В отличие от[MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.md), цей метод ініціалізуватиме підключення до бази даних і при необхідності виконувати виявлення сервера. Детальніше дивіться . [» Специфікацію вибору сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst#single-threaded-server-selection)

### Список параметрів

`readPreference` [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)) .

Перевага читання використовується для вибору сервера. Якщо **`null`** або опущено, за промовчанням буде обрано первинний сервер.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.md), Що відповідає перевагу читання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   При неможливості знайти сервер, що відповідає перевагу читання, викидає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.11.0 | Параметр`readPreference` тепер необов'язковий. Якщо вказано значення **`null`** або опущено, за промовчанням буде обрано первинний сервер. |

### Дивіться також

-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.md)
-   [MongoDB\\Driver\\Manager::getServers()](mongodb-driver-manager.getservers.md) \- Повертає сервери, до яких підключено менеджера
-   [» Специфікація вибору сервера](https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst)
