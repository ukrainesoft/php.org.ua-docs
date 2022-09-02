---
navigation:
  - mongodb-bson-javascript.getscope.md: '« MongoDBBSONJavascript::getScope'
  - mongodb-bson-javascript.serialize.md: 'MongoDBBSONJavascript::serialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDBBSONJavascript
title: 'MongoDBBSONJavascript::jsonSerialize'
---
# MongoDBBSONJavascript::jsonSerialize

(mongodb >=1.2.0)

MongoDBBSONJavascript::jsonSerialize — Повертає уявлення, яке може бути перетворене на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані [jsonencode()](function.json-encode.md) для створення JSON-подання [MongoDBBSONJavascript](class.mongodb-bson-javascript.md)

> **Зауваження**: Висновок відповідає висновку функції [MongoDBBSONtoJSON()](function.mongodb.bson-tojson.md)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) і [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.md) - Задає дані, які мають бути серіалізовані у JSON
-   [jsonencode()](function.json-encode.md) - Повертає JSON-подання даних
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) - Повертає Relaxed Extended JSON подання значення BSON
-   [» Розширений JSON MongoDB](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
