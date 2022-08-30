Повертає уявлення, яке може бути перетворено на JSON

-   [« MongoDBBSONJavascript::getScope](mongodb-bson-javascript.getscope.html)
    
-   [MongoDBBSONJavascript::serialize »](mongodb-bson-javascript.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)
    
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

Повертає дані, які можуть бути серіалізовані [jsonencode()](function.json-encode.html) для створення JSON-подання [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)

> **Зауваження**: Висновок відповідає висновку функції [MongoDBBSONtoJSON()](function.mongodb.bson-tojson.html)яка використовує успадкований, специфічний для драйвера, розширений формат JSON. Він не обов'язково підходитиме під [» relaxed](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example) або [» canonical](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) уявлення розширеного JSON, що використовуються в [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) і [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html)відповідно.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.html) - Задає дані, які мають бути серіалізовані у JSON
-   [jsonencode()](function.json-encode.html) - Повертає JSON-подання даних
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) - Повертає Relaxed Extended JSON подання значення BSON
-   [» Расширенный JSON MongoDB](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)