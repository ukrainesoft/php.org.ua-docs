---
navigation:
  - mongodb-driver-serverdescription.getlastupdatetime.md: '« MongoDB\\Driver\\ServerDescription::getLastUpdateTime'
  - mongodb-driver-serverdescription.getroundtriptime.md: 'MongoDB\\Driver\\ServerDescription::getRoundTripTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription
title: 'MongoDB\\Driver\\ServerDescription::getPort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerDescription::getPort

(mongodb >=1.13.0)

MongoDB\\Driver\\ServerDescription::getPort — Повертає порт, на якому прослуховується цей сервер

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getPort(): int
```

Повертає порт, на якому прослуховується сервер.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає порт, на якому прослуховується сервер.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getPort()](mongodb-driver-server.getport.md) \- Повертає порт, який слухає сервер
