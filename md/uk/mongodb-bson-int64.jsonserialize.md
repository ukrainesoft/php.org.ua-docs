---
navigation:
  - mongodb-bson-int64.construct.md: '« MongoDBBSONInt64::construct'
  - mongodb-bson-int64.serialize.md: 'MongoDBBSONInt64::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDBBSONInt64
title: 'MongoDBBSONInt64::jsonSerialize'
---
# MongoDBBSONInt64::jsonSerialize

(mongodb >=1.5.0)

MongoDBBSONInt64::jsonSerialize — Повертає уявлення, яке можна перетворити на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані за допомогою [jsonencode()](function.json-encode.md) для створення розширеного JSON-подання [MongoDBBSONInt64](class.mongodb-bson-int64.md)

> **Зауваження**: Висновок відповідає функції [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md), яка використовує [» канонічний](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) Розширений формат JSON. Це відрізняється від інших класів BSON, які використовують застарілий розширений формат JSON для конкретного драйвера ([MongoDBBSONtoJSON()](function.mongodb.bson-tojson.md)), щоб забезпечити правильне подання 64-розрядного цілого чисельного значення на 32-розрядних платформах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) - Задає дані, які мають бути серіалізовані у JSON
-   [jsonencode()](function.json-encode.md) - Повертає JSON-подання даних
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) - Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
