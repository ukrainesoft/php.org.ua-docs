---
navigation:
  - function.mongodb.bson-tocanonicalextendedjson.html: « MongoDBBSONtoCanonicalExtendedJSON
  - function.mongodb.bson-tophp.html: MongoDBBSONtoPHP »
  - index.md: PHP Manual
  - ref.bson.functions.md: Функції
title: MongoDBBSONtoJSON
---
# MongoDBBSONtoJSON

(mongodb >=1.0.0)

MongoDBBSONtoJSON — Повертає Legacy Extended JSON подання значення BSON

### Опис

```methodsynopsis
MongoDB\BSON\toJSON(string $bson): string
```

Перетворює рядок BSON на його [» Legacy Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/) уявлення.

> **Зауваження**: Існує кілька форматів JSON для представлення BSON Ця функція реалізує "суворий режим", визначений у [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/), який був замінений канонічними та спрощеними форматами, визначеними в [» Спецификации Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst) та реалізованими [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) і [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) відповідно.

**Увага**

[» JSON](http://www.json.org/) не підтримує [**`NAN`**](language.types.float.html#language.types.float.nan) і [**`INF`**](function.is-infinite.html), а формат Legacy Extended JSON MongoDB не визначає альтернативного представлення для цих значень ([» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson) виводитиме літерали `nan` і `inf`, які можуть не розпізнатися як коректний JSON). Якщо ви працюєте з BSON, який може містити нескінченні числа, використовуйте [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) або [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md)

### Список параметрів

`bson` (string)

Значення BSON для перетворення.

### Значення, що повертаються

Перетворене значення JSON.

### Помилки

-   Виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md) викидається, якщо вхідні дані не є одним документом BSON. Можливі причини включають, але не обмежені некоректним BSON, зайвими даними або несподіваною помилкою [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONtoJSON()****

```php
<?php

$documents = [
    [ 'null' => null ],
    [ 'boolean' => true ],
    [ 'string' => 'foo' ],
    [ 'int32' => 123 ],
    [ 'int64' => 4294967295 ],
    [ 'double' => 1.0, ],
    [ 'nan' => NAN ],
    [ 'pos_inf' => INF ],
    [ 'neg_inf' => -INF ],
    [ 'array' => [ 'foo', 'bar' ]],
    [ 'document' => [ 'foo' => 'bar' ]],
    [ 'oid' => new MongoDB\BSON\ObjectId('56315a7c6118fd1b920270b1') ],
    [ 'dec128' => new MongoDB\BSON\Decimal128('1234.5678') ],
    [ 'binary' => new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC) ],
    [ 'date' => new MongoDB\BSON\UTCDateTime(1445990400000) ],
    [ 'timestamp' => new MongoDB\BSON\Timestamp(1234, 5678) ],
    [ 'regex' => new MongoDB\BSON\Regex('pattern', 'i') ],
    [ 'code' => new MongoDB\BSON\Javascript('function() { return 1; }') ],
    [ 'code_ws' => new MongoDB\BSON\Javascript('function() { return a; }', ['a' => 1]) ],
    [ 'minkey' => new MongoDB\BSON\MinKey ],
    [ 'maxkey' => new MongoDB\BSON\MaxKey ],
];

foreach ($documents as $document) {
    $bson = MongoDB\BSON\fromPHP($document);
    echo MongoDB\BSON\toJSON($bson), "\n";
}

?>
```

Результат виконання цього прикладу:

```
{ "null" : null }
{ "boolean" : true }
{ "string" : "foo" }
{ "int32" : 123 }
{ "int64" : 4294967295 }
{ "double" : 1.0 }
{ "nan" : nan }
{ "pos_inf" : inf }
{ "neg_inf" : -inf }
{ "array" : [ "foo", "bar" ] }
{ "document" : { "foo" : "bar" } }
{ "oid" : { "$oid" : "56315a7c6118fd1b920270b1" } }
{ "dec128" : { "$numberDecimal" : "1234.5678" } }
{ "binary" : { "$binary" : "Zm9v", "$type" : "00" } }
{ "date" : { "$date" : 1445990400000 } }
{ "timestamp" : { "$timestamp" : { "t" : 5678, "i" : 1234 } } }
{ "regex" : { "$regex" : "pattern", "$options" : "i" } }
{ "code" : { "$code" : "function() { return 1; }" } }
{ "code_ws" : { "$code" : "function() { return a; }", "$scope" : { "a" : 1 } } }
{ "minkey" : { "$minKey" : 1 } }
{ "maxkey" : { "$maxKey" : 1 } }
```

### Дивіться також

-   [MongoDBBSONfromJSON()](function.mongodb.bson-fromjson.md) - Повертає подання BSON значення JSON
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.md) - Повертає Canonical Extended JSON подання для значення BSON
-   [MongoDBBSONtoRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) - Повертає Relaxed Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
