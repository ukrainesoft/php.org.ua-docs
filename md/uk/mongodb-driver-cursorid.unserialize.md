---
navigation:
  - mongodb-driver-cursorid.tostring.md: '« MongoDB\\Driver\\CursorId::\_\_function toString() { [native code] }'
  - class.mongodb-driver-cursorinterface.md: MongoDB\\Driver\\CursorInterface »
  - index.md: PHP Manual
  - class.mongodb-driver-cursorid.md: MongoDB\\Driver\\CursorId
title: 'MongoDB\\Driver\\CursorId::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorId::unserialize

(mongodb >=1.7.0)

MongoDB\\Driver\\CursorId::unserialize — Десеріалізація CursorId

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::unserialize(string $data): void
```

### Список параметрів

`data`

Серіалізований [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Кидає виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)якщо виникла неможливо зробити десеріалізацію властивості, наприклад, якщо значення`serialized`не коректно.
-   Кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо властивості не коректні, наприклад, пропущені поля або вони мають некоректні значення.

### Дивіться також

-   [MongoDB\\Driver\\CursorId::serialize()](mongodb-driver-cursorid.serialize.md) \- Серіалізація CursorId
-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [Серіалізація об'єктів](language.oop5.serialization.md)
