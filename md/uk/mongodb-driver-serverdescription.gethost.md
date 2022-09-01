---
navigation:
  - mongodb-driver-serverdescription.gethelloresponse.html: '« MongoDBDriverServerDescription::getHelloResponse'
  - mongodb-driver-serverdescription.getlastupdatetime.html: 'MongoDBDriverServerDescription::getLastUpdateTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.html: MongoDBDriverServerDescription
title: 'MongoDBDriverServerDescription::getHost'
---
# MongoDBDriverServerDescription::getHost

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getHost — Повертає ім'я сервера.

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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverServer::getHost()](mongodb-driver-server.gethost.html) - Повертає ім'я сервера хоста
