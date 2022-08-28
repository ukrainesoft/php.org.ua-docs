Повертає уявлення, яке можна перетворити на JSON

-   [« MongoDB\\BSON\\Int64::\_\_construct](mongodb-bson-int64.construct.html)
    
-   [MongoDB\\BSON\\Int64::serialize »](mongodb-bson-int64.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html)
    
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

Повертає дані, які можуть бути серіалізовані за допомогою [json\_encode()](function.json-encode.html) для створення розширеного JSON-подання [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html)

> **Зауваження**: Висновок відповідає функції [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html), яка використовує [» канонический](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example) Розширений формат JSON. Це відрізняється від інших класів BSON, які використовують застарілий розширений формат JSON для конкретного драйвера ([MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.html)), щоб забезпечити правильне подання 64-розрядного цілого чисельного значення на 32-розрядних платформах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [JsonSerializable::jsonSerialize()](jsonserializable.jsonserialize.html) - Задає дані, які мають бути серіалізовані у JSON
-   [json\_encode()](function.json-encode.html) - Повертає JSON-подання даних
-   [MongoDB\\BSON\\toCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.html) - Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)