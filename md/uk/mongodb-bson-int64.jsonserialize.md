---
navigation:
  - mongodb-bson-int64.construct.md: '« MongoDB\\BSON\\Int64::\_\_construct'
  - mongodb-bson-int64.serialize.md: 'MongoDB\\BSON\\Int64::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-int64.md: MongoDB\\BSON\\Int64
title: 'MongoDB\\BSON\\Int64::jsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Int64::jsonSerialize

(mongodb >=1.5.0)

MongoDB\\BSON\\Int64::jsonSerialize — Повертає уявлення, яке можна перетворити на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Int64::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані за допомогою [json\_encode()](function.json-encode.md)для создания расширенного JSON-представления[MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

> **Зауваження**: Висновок відповідає функції [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md), яка використовує [» канонічний](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) Розширений формат JSON. Це відрізняється від інших класів BSON, які використовують застарілий розширений формат JSON для конкретного драйвера ([MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.md)), щоб забезпечити правильне подання 64-розрядного цілого чисельного значення на 32-розрядних платформах.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) \- Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) \- Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) \- Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
