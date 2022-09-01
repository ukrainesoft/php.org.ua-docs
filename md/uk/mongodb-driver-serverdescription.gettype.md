---
navigation:
  - mongodb-driver-serverdescription.getroundtriptime.html: '« MongoDBDriverServerDescription::getRoundTripTime'
  - class.mongodb-driver-topologydescription.html: MongoDBDriverTopologyDescription »
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.html: MongoDBDriverServerDescription
title: 'MongoDBDriverServerDescription::getType'
---
# MongoDBDriverServerDescription::getType

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getType — Повертає рядок, який позначає тип сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getType(): string
```

Повертає рядок (string), що позначає тип сервера. Значення співвідноситиметься з константою [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що позначає тип сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverServer::getType()](mongodb-driver-server.gettype.md) - Повертає ціле число, що означає тип цього сервера
