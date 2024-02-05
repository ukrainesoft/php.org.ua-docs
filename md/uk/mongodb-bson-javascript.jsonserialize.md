---
navigation:
  - mongodb-bson-javascript.getscope.md: '« MongoDB\\BSON\\Javascript::getScope'
  - mongodb-bson-javascript.serialize.md: 'MongoDB\\BSON\\Javascript::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::jsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::jsonSerialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Javascript::jsonSerialize — Повертає уявлення, яке може бути перетворене на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані [json\_encode()](function.json-encode.md)для создания JSON-представления[MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.md)

> **Зауваження**: Висновок відповідає висновку функції [MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.md)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) і [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) \- Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) \- Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) \- Повертає Relaxed Extended JSON подання значення BSON
-   [» Розширений JSON MongoDB](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
