---
navigation:
  - mongodb-driver-server.getport.md: '« MongoDB\\Driver\\Server::getPort'
  - mongodb-driver-server.gettags.md: 'MongoDB\\Driver\\Server::getTags »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getServerDescription'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getServerDescription

(mongodb >=1.13.0)

MongoDB\\Driver\\Server::getServerDescription — Повертає ServerDescription сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getServerDescription(): MongoDB\Driver\ServerDescription
```

Повертає [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md) сервера. Це незмінний об'єкт значення, який описуватиме сервер під час виклику методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md)сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
