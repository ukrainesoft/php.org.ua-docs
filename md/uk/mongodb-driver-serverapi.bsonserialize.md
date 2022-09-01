---
navigation:
  - class.mongodb-driver-serverapi.html: « MongoDBDriverServerApi
  - mongodb-driver-serverapi.construct.html: 'MongoDBDriverServerApi::construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.html: MongoDBDriverServerApi
title: 'MongoDBDriverServerApi::bsonSerialize'
---
# MongoDBDriverServerApi::bsonSerialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::bsonSerialize — Повертає об'єкт для серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::bsonSerialize(): object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт для серіалізації ServerApi як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) - Надає масив або документ для серіалізації у BSON
