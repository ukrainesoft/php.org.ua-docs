---
navigation:
  - mongodb-driver-serverdescription.getport.md: '« MongoDBDriverServerDescription::getPort'
  - mongodb-driver-serverdescription.gettype.md: 'MongoDBDriverServerDescription::getType »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDBDriverServerDescription
title: 'MongoDBDriverServerDescription::getRoundTripTime'
---
# MongoDBDriverServerDescription::getRoundTripTime

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getRoundTripTime — Повертає час обходу сервера в мілісекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getRoundTripTime(): ?int
```

Повертає час обходу сервера у мілісекундах. Це вимір тривалості команди [» hello](https://www.mongodb.com/docs/manual/reference/command/hello/)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час обходу сервера у мілісекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getLatency()](mongodb-driver-server.getlatency.md) - Повертає затримку сервера у мілісекундах
