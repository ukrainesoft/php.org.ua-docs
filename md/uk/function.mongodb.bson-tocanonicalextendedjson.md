---
navigation:
  - function.mongodb.bson-fromphp.md: « MongoDB\\BSON\\fromPHP
  - function.mongodb.bson-tojson.md: MongoDB\\BSON\\toJSON »
  - index.md: PHP Manual
  - ref.bson.functions.md: Функції
title: MongoDB\\BSON\\toCanonicalExtendedJSON
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\toCanonicalExtendedJSON

(mongodb >=1.3.0)

MongoDB\\BSON\\toCanonicalExtendedJSON — Повертає Canonical Extended JSON подання для значення BSON

### Опис

```methodsynopsis
MongoDB\BSON\toCanonicalExtendedJSON(string $bson): string
```

Перетворює рядок BSON на його [» Canonical Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example)\-уявлення. Канонічний формат віддає перевагу точності типів за рахунок короткого виводу і найбільш підходить для створення вихідних даних, які можуть бути перетворені назад в BSON без будь-якої втрати інформації про тип (наприклад, числові типи залишаться диференційованими).

### Список параметрів

`bson`(string)

Значення BSON для перетворення.

### Значення, що повертаються

Перетворене значення JSON.

### Помилки

-   Исключение[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)викидається, якщо вхідні дані не є одним документом BSON. Можливі причини включають, але не обмежені некоректним BSON, зайвими даними або несподіваною помилкою[» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\toCanonicalExtendedJSON()\*\*\*\*

```php
<?php

$documents = [
    [ 'null' => null ],
    [ 'boolean' => true ],
    [ 'string' => 'foo' ],
    [ 'int32' => 123 ],
    [ 'int64' => 4294967295 ],
    [ 'double' => 1.0, ],
    [ 'nan' => NAN ],
    [ 'pos_inf' => INF ],
    [ 'neg_inf' => -INF ],
    [ 'array' => [ 'foo', 'bar' ]],
    [ 'document' => [ 'foo' => 'bar' ]],
    [ 'oid' => new MongoDB\BSON\ObjectId('56315a7c6118fd1b920270b1') ],
    [ 'dec128' => new MongoDB\BSON\Decimal128('1234.5678') ],
    [ 'binary' => new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC) ],
    [ 'date' => new MongoDB\BSON\UTCDateTime(1445990400000) ],
    [ 'timestamp' => new MongoDB\BSON\Timestamp(1234, 5678) ],
    [ 'regex' => new MongoDB\BSON\Regex('pattern', 'i') ],
    [ 'code' => new MongoDB\BSON\Javascript('function() { return 1; }') ],
    [ 'code_ws' => new MongoDB\BSON\Javascript('function() { return a; }', ['a' => 1]) ],
    [ 'minkey' => new MongoDB\BSON\MinKey ],
    [ 'maxkey' => new MongoDB\BSON\MaxKey ],
];

foreach ($documents as $document) {
    $bson = MongoDB\BSON\fromPHP($document);
    echo MongoDB\BSON\toCanonicalExtendedJSON($bson), "\n";
}

?>
```

Результат виконання наведеного прикладу:

```
{ "null" : null }
{ "boolean" : true }
{ "string" : "foo" }
{ "int32" : { "$numberInt" : "123" } }
{ "int64" : { "$numberLong" : "4294967295"} }
{ "double" : { "$numberDouble" : "1.0" } }
{ "nan" : { "$numberDouble" : "NaN" } }
{ "pos_inf" : { "$numberDouble" : "Infinity" } }
{ "neg_inf" : { "$numberDouble" : "-Infinity" } }
{ "array" : [ "foo", "bar" ] }
{ "document" : { "foo" : "bar" } }
{ "oid" : { "$oid" : "56315a7c6118fd1b920270b1" } }
{ "dec128" : { "$numberDecimal" : "1234.5678" } }
{ "binary" : { "$binary" : { "base64": "Zm9v", "subType" : "00" } } }
{ "date" : { "$date" : { "$numberLong" : "1445990400000" } } }
{ "timestamp" : { "$timestamp" : { "t" : 5678, "i" : 1234 } } }
{ "regex" : { "$regularExpression" : { "pattern" : "pattern", "options" : "i" } } }
{ "code" : { "$code" : "function() { return 1; }" } }
{ "code_ws" : { "$code" : "function() { return a; }", "$scope" : { "a" : { "$numberInt" : "1" } } } }
{ "minkey" : { "$minKey" : 1 } }
{ "maxkey" : { "$maxKey" : 1 } }
```

### Дивіться також

-   [MongoDB\\BSON\\Document::fromJSON()](mongodb-bson-document.fromjson.md) \- Створює новий екземпляр документа з рядка JSON
-   [MongoDB\\BSON\\Document::toCanonicalExtendedJSON()](mongodb-bson-document.tocanonicalextendedjson.md) \- Повертає Canonical Extended JSON-подання BSON-документу
-   [MongoDB\\BSON\\fromJSON()](function.mongodb.bson-fromjson.md) \- Повертає подання BSON значення JSON
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) \- Повертає Relaxed Extended JSON подання значення BSON
-   [» Специфікація Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst)
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
