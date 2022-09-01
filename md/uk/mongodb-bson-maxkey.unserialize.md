---
navigation:
  - mongodb-bson-maxkey.serialize.html: '« MongoDBBSONMaxKey::serialize'
  - class.mongodb-bson-minkey.html: MongoDBBSONMinKey »
  - index.html: PHP Manual
  - class.mongodb-bson-maxkey.html: MongoDBBSONMaxKey
title: 'MongoDBBSONMaxKey::unserialize'
---
# MongoDBBSONMaxKey::unserialize

(mongodb >=1.2.0)

MongoDBBSONMaxKey::unserialize — Десеріалізує MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONMaxKey::serialize()](mongodb-bson-maxkey.serialize.md) - Серіалізує MaxKey
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
