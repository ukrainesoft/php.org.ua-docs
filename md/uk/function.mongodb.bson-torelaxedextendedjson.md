---
navigation:
  - function.mongodb.bson-tophp.html: « MongoDBBSONtoPHP
  - class.mongodb-bson-binary.html: MongoDBBSONBinary »
  - index.html: PHP Manual
  - ref.bson.functions.html: Функції
title: MongoDBBSONtoRelaxedExtendedJSON
---
# MongoDBBSONtoRelaxedExtendedJSON

(mongodb >=1.3.0)

MongoDBBSONtoRelaxedExtendedJSON — Повертає Relaxed Extended JSON подання значення BSON

### Опис

```methodsynopsis
MongoDB\BSON\toRelaxedExtendedJSON(string $bson): string
```

Перетворює рядок BSON на її подання [» Relaxed Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example). Розслаблений формат надає перевагу використанню примітивів типу JSON за рахунок точності типів і найбільше підходить для отримання вихідних даних, які можуть бути легко використані веб-API та людьми.

### Список параметрів

`bson` (string)

Значення BSON для перетворення.

### Значення, що повертаються

Перетворене значення JSON.

### Помилки

-   Виняток [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) викидається, якщо вхідні дані не є одним документом BSON. Можливі причини включають, але не обмежені некоректним BSON, зайвими даними або несподіваною помилкою [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONtoRelaxedExtendedJSON()****

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
    echo MongoDB\BSON\toRelaxedExtendedJSON($bson), "\n";
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
{ "nan" : { "$numberDouble" : "NaN" } }
{ "pos_inf" : { "$numberDouble" : "Infinity" } }
{ "neg_inf" : { "$numberDouble" : "-Infinity" } }
{ "array" : [ "foo", "bar" ] }
{ "document" : { "foo" : "bar" } }
{ "oid" : { "$oid" : "56315a7c6118fd1b920270b1" } }
{ "dec128" : { "$numberDecimal" : "1234.5678" } }
{ "binary" : { "$binary" : { "base64": "Zm9v", "subType" : "00" } } }
{ "date" : { "$date" : "2015-10-28T00:00:00Z" } }
{ "timestamp" : { "$timestamp" : { "t" : 5678, "i" : 1234 } } }
{ "regex" : { "$regularExpression" : { "pattern" : "pattern", "options" : "i" } } }
{ "code" : { "$code" : "function() { return 1; }" } }
{ "code_ws" : { "$code" : "function() { return a; }", "$scope" : { "a" : 1 } } }
{ "minkey" : { "$minKey" : 1 } }
{ "maxkey" : { "$maxKey" : 1 } }
```

### Дивіться також

-   [MongoDBBSONfromJSON()](function.mongodb.bson-fromjson.html) - Повертає подання BSON значення JSON
-   [MongoDBBSONtoCanonicalExtendedJSON()](function.mongodb.bson-tocanonicalextendedjson.html) - Повертає Canonical Extended JSON подання для значення BSON
-   [» Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst)
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
