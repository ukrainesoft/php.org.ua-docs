---
navigation:
  - mongodb-bson-undefined.tostring.md: '« MongoDBBSONUndefined::toString'
  - mongodb.monitoring.md: MongoDBDriverMonitoring »
  - index.md: PHP Manual
  - class.mongodb-bson-undefined.md: MongoDBBSONUndefined
title: 'MongoDBBSONUndefined::unserialize'
---
# MongoDBBSONUndefined::unserialize

(mongodb >=1.4.0)

MongoDBBSONUndefined::unserialize — Десеріалізує Undefined

### Опис

```methodsynopsis
final public MongoDB\BSON\Undefined::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDBBSONUndefined](class.mongodb-bson-undefined.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBBSONUndefined::serialize()](mongodb-bson-undefined.serialize.md) - Серіалізує Undefined
-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
