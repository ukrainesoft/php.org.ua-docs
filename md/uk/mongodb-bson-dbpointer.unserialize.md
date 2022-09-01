---
navigation:
  - mongodb-bson-dbpointer.tostring.html: '« MongoDBBSONDBPointer::toString'
  - class.mongodb-bson-int64.html: MongoDBBSONInt64 »
  - index.md: PHP Manual
  - class.mongodb-bson-dbpointer.html: MongoDBBSONDBPointer
title: 'MongoDBBSONDBPointer::unserialize'
---
# MongoDBBSONDBPointer::unserialize

(mongodb >=1.4.0)

MongoDBBSONDBPointer::unserialize — Десеріалізує DBPointer

### Опис

```methodsynopsis
final public MongoDB\BSON\DBPointer::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONDBPointer](class.mongodb-bson-dbpointer.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBBSONDBPointer::serialize()](mongodb-bson-dbpointer.serialize.html) - Серіалізує DBPointer
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
