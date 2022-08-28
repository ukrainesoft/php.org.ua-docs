Повертає уявлення, яке може бути перетворено на JSON

-   [« MongoDB\\BSON\\Javascript::getScope](mongodb-bson-javascript.getscope.html)
    
-   [MongoDB\\BSON\\Javascript::serialize »](mongodb-bson-javascript.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.html)
    
-   Повертає уявлення, яке може бути перетворено на JSON
    

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

Повертає дані, які можуть бути серіалізовані [json\_encode()](function.json-encode.html) для створення JSON-подання [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.html)

> **Зауваження**: Висновок відповідає висновку функції [MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.html)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) і [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.html) - Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.html) - Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) - Повертає Relaxed Extended JSON подання значення BSON
-   [» Расширенный JSON MongoDB](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)