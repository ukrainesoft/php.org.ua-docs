---
navigation:
  - mongodb-driver-serverdescription.getport.md: '« MongoDB\\Driver\\ServerDescription::getPort'
  - mongodb-driver-serverdescription.gettype.md: 'MongoDB\\Driver\\ServerDescription::getType »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription
title: 'MongoDB\\Driver\\ServerDescription::getRoundTripTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerDescription::getRoundTripTime

(mongodb >=1.13.0)

MongoDB\\Driver\\ServerDescription::getRoundTripTime — Повертає час обходу сервера в мілісекундах

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getLatency()](mongodb-driver-server.getlatency.md) \- Повертає затримку сервера у мілісекундах
