Повертає уявлення, яке можна перетворити на JSON

-   [« MongoDB\\BSON\\ObjectId::getTimestamp](mongodb-bson-objectid.gettimestamp.html)
    
-   [MongoDB\\BSON\\ObjectId::serialize »](mongodb-bson-objectid.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)
    
-   Повертає уявлення, яке можна перетворити на JSON
    

# MongoDBBSONObjectId::jsonSerialize

(mongodb >=1.2.0)

MongoDBBSONObjectId::jsonSerialize — Повертає уявлення, яке можна перетворити на JSON

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::jsonSerialize(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дані, які можуть бути серіалізовані за допомогою [json\_encode()](function.json-encode.html) для створення розширеного JSON-подання [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)

> **Зауваження**: Висновок відповідає висновку функції [MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.html)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) і [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.html) - Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.html) - Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) - Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)