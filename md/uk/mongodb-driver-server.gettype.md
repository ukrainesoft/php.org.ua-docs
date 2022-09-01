---
navigation:
  - mongodb-driver-server.gettags.html: '« MongoDBDriverServer::getTags'
  - mongodb-driver-server.isarbiter.html: 'MongoDBDriverServer::isArbiter »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.html: MongoDBDriverServer
title: 'MongoDBDriverServer::getType'
---
# MongoDBDriverServer::getType

(mongodb >=1.0.0)

MongoDBDriverServer::getType — Повертає ціле число, яке означає тип цього сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getType(): int
```

Повертає int, що означає тип цього сервера. Значення буде відповідати константі [MongoDBDriverServer](class.mongodb-driver-server.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає int, що означає тип цього сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getInfo()](mongodb-driver-server.getinfo.html) - Повертає масив інформації, що описує сервер
-   [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html) - Повертає рядок, що позначає тип сервера
