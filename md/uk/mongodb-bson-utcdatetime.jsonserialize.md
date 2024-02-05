---
navigation:
  - mongodb-bson-utcdatetime.construct.md: '« MongoDB\\BSON\\UTCDateTime::\_\_construct'
  - mongodb-bson-utcdatetime.serialize.md: 'MongoDB\\BSON\\UTCDateTime::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime
title: 'MongoDB\\BSON\\UTCDateTime::jsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\UTCDateTime::jsonSerialize

(mongodb >=1.2.0)

MongoDB\\BSON\\UTCDateTime::jsonSerialize — Повертає уявлення, яке можна перетворити на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані за допомогою [json\_encode()](function.json-encode.md)для создания расширенного JSON-представления[MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.md)

> **Зауваження**: Висновок відповідає висновку функції [MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.md)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) і [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) \- Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) \- Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) \- Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
