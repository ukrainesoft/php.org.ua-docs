---
navigation:
  - mongodb-bson-timestamp.gettimestamp.html: '« MongoDBBSONTimestamp::getTimestamp'
  - mongodb-bson-timestamp.serialize.html: 'MongoDBBSONTimestamp::serialize »'
  - index.html: PHP Manual
  - class.mongodb-bson-timestamp.html: MongoDBBSONTimestamp
title: 'MongoDBBSONTimestamp::jsonSerialize'
---
# MongoDBBSONTimestamp::jsonSerialize

(mongodb >=1.2.0)

MongoDBBSONTimestamp::jsonSerialize — Повертає уявлення, яке можна перетворити на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані за допомогою [jsonencode()](function.json-encode.html) для створення розширеного JSON-подання [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.md)

> **Зауваження**: Висновок відповідає висновку функції [MongoDBBSONtoJSON()](function.mongodb.bson-tojson.html)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) і [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) - Задає дані, які мають бути серіалізовані у JSON
-   [jsonencode()](function.json-encode.md) - Повертає JSON-подання даних
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) - Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
