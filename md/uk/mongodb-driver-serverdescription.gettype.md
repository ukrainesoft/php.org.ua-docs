---
navigation:
  - mongodb-driver-serverdescription.getroundtriptime.md: '« MongoDB\\Driver\\ServerDescription::getRoundTripTime'
  - class.mongodb-driver-topologydescription.md: MongoDB\\Driver\\TopologyDescription »
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription
title: 'MongoDB\\Driver\\ServerDescription::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerDescription::getType

(mongodb >=1.13.0)

MongoDB\\Driver\\ServerDescription::getType — Повертає рядок, який позначає тип сервера

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getType(): string
```

Повертає рядок (string), що позначає тип сервера. Значення співвідноситиметься з константою [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що позначає тип сервера.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Server::getType()](mongodb-driver-server.gettype.md) \- Повертає ціле число, що означає тип цього сервера
