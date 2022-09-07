---
navigation:
  - mongodb-bson-minkey.serialize.md: '« MongoDBBSONMinKey::serialize'
  - class.mongodb-bson-objectid.md: MongoDBBSONObjectId »
  - index.md: PHP Manual
  - class.mongodb-bson-minkey.md: MongoDBBSONMinKey
title: 'MongoDBBSONMinKey::unserialize'
---
# MongoDBBSONMinKey::unserialize

(mongodb >=1.2.0)

MongoDBBSONMonKey::unserialize — Десеріалізує MonKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONMinKey](class.mongodb-bson-minkey.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONMinKey::serialize()](mongodb-bson-minkey.serialize.md) - Серіалізує MinKey
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
