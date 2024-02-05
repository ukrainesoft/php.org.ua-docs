---
navigation:
  - class.mongodb-driver-serverapi.md: « MongoDB\\Driver\\ServerApi
  - mongodb-driver-serverapi.construct.md: 'MongoDB\\Driver\\ServerApi::\_\_construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.md: MongoDB\\Driver\\ServerApi
title: 'MongoDB\\Driver\\ServerApi::bsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerApi::bsonSerialize

(mongodb >=1.10.0)

MongoDB\\Driver\\ServerApi::bsonSerialize — Повертає об'єкт для серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::bsonSerialize(): stdClass
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт для серіалізації ServerApi як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) \- Надає масив або документ для серіалізації у BSON
