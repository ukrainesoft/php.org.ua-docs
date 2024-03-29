---
navigation:
  - mongodb-driver-serverdescription.gethelloresponse.md: '« MongoDB\\Driver\\ServerDescription::getHelloResponse'
  - mongodb-driver-serverdescription.getlastupdatetime.md: 'MongoDB\\Driver\\ServerDescription::getLastUpdateTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription
title: 'MongoDB\\Driver\\ServerDescription::getHost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerDescription::getHost

(mongodb >=1.13.0)

MongoDB\\Driver\\ServerDescription::getHost — Повертає ім'я сервера.

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getHost(): string
```

Повертає ім'я сервера хоста.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я сервера хоста.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getHost()](mongodb-driver-server.gethost.md) \- Повертає ім'я сервера хоста
