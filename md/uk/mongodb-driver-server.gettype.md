---
navigation:
  - mongodb-driver-server.gettags.md: '« MongoDB\\Driver\\Server::getTags'
  - mongodb-driver-server.isarbiter.md: 'MongoDB\\Driver\\Server::isArbiter »'
  - index.md: PHP Manual
  - class.mongodb-driver-server.md: MongoDB\\Driver\\Server
title: 'MongoDB\\Driver\\Server::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Server::getType

(mongodb >=1.0.0)

MongoDB\\Driver\\Server::getType — Повертає ціле число, яке означає тип цього сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\Server::getType(): int
```

Повертає int, що означає тип цього сервера. Значення буде відповідати константі [MongoDB\\Driver\\Server](class.mongodb-driver-server.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає int, що означає тип цього сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getInfo()](mongodb-driver-server.getinfo.md) \- Повертає масив інформації, що описує сервер
-   [MongoDB\\Driver\\ServerDescription::getType()](mongodb-driver-serverdescription.gettype.md) \- Повертає рядок, що позначає тип сервера
