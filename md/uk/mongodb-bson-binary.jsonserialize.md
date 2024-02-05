---
navigation:
  - mongodb-bson-binary.gettype.md: '« MongoDB\\BSON\\Binary::getType'
  - mongodb-bson-binary.serialize.md: 'MongoDB\\BSON\\Binary::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-binary.md: MongoDB\\BSON\\Binary
title: 'MongoDB\\BSON\\Binary::jsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Binary::jsonSerialize

(mongodb >=1.2.0)

MongoDB\\BSON\\Binary::jsonSerialize — Повертає уявлення, яке можна перетворити на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Binary::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можна серіалізувати за допомогою [json\_encode()](function.json-encode.md)для создания расширенного JSON-представления[MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)

> **Зауваження**: Висновок відповідає висновку функції [MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.md)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) і [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) \- Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) \- Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) \- Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
