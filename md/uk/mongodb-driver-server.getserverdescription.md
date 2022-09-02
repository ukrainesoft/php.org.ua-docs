---
navigation:
  - mongodb-driver-server.getport.md: '« MongoDBDriverServer::getPort'
  - mongodb-driver-server.gettags.md: 'MongoDBDriverServer::getTags »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDBDriverServer
title: 'MongoDBDriverServer::getServerDescription'
---
# MongoDBDriverServer::getServerDescription

(mongodb >=1.13.0)

MongoDBDriverServer::getServerDescription — Повертає ServerDescription сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getServerDescription(): MongoDB\Driver\ServerDescription
```

Повертає [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.md) сервера. Це незмінний об'єкт значення, який описуватиме сервер під час виклику методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.md) сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
