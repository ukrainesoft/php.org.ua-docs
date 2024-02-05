---
navigation:
  - mongodb-driver-cursorid.construct.md: '« MongoDB\\Driver\\CursorId::\_\_construct'
  - mongodb-driver-cursorid.tostring.md: 'MongoDB\\Driver\\CursorId::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorid.md: MongoDB\\Driver\\CursorId
title: 'MongoDB\\Driver\\CursorId::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorId::serialize

(mongodb >=1.7.0)

MongoDB\\Driver\\CursorId::serialize — Серіалізація CursorId

### Опис

```methodsynopsis
final public MongoDB\Driver\CursorId::serialize(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает сериализованное представление[MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\CursorId::unserialize()](mongodb-driver-cursorid.unserialize.md) \- Десеріалізація CursorId
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
