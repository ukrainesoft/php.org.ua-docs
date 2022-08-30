Повертає уявлення, яке можна перетворити на JSON

-   [« MongoDBBSONInt64::construct](mongodb-bson-int64.construct.html)
    
-   [MongoDBBSONInt64::serialize »](mongodb-bson-int64.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONInt64](class.mongodb-bson-int64.html)
    
-   Повертає уявлення, яке можна перетворити на JSON
    

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

Повертає дані, які можуть бути серіалізовані за допомогою [jsonencode()](function.json-encode.html) для створення розширеного JSON-подання [MongoDBBSONInt64](class.mongodb-bson-int64.html)

> **Зауваження**: Висновок відповідає функції [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html), яка використовує [» канонічний](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) Розширений формат JSON. Це відрізняється від інших класів BSON, які використовують застарілий розширений формат JSON для конкретного драйвера ([MongoDBBSONtoJSON()](function.mongodb.bson-tojson.html)), щоб забезпечити правильне подання 64-розрядного цілого чисельного значення на 32-розрядних платформах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.html) - Задає дані, які мають бути серіалізовані у JSON
-   [jsonencode()](function.json-encode.html) - Повертає JSON-подання даних
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) - Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)