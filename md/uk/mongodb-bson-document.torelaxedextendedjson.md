---
navigation:
  - mongodb-bson-document.tophp.md: '« MongoDB\\BSON\\Document::toPHP'
  - mongodb-bson-document.tostring.md: 'MongoDB\\BSON\\Document::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-document.md: MongoDB\\BSON\\Document
title: 'MongoDB\\BSON\\Document::toRelaxedExtendedJSON'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Document::toRelaxedExtendedJSON

(mongodb >=1.16.0)

MongoDB\\BSON\\Document::toRelaxedExtendedJSON — Повертає Relaxed Extended JSON подання BSON-документу

### Опис

```methodsynopsis
final public MongoDB\BSON\Document::toRelaxedExtendedJSON(): string
```

Перетворює BSON-документ на подання [» Relaxed Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example). Формат Relaxed воліє використовувати примітиви типів JSON на шкоду вірності типів і найбільше підходить для створення висновку, який може бути легко використаний веб-інтерфейсами та людьми.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Document::toRelaxedExtendedJSON()\*\*\*\*

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
    $bson = MongoDB\BSON\Document::fromPHP($document);
    echo $bson->toRelaxedExtendedJSON(), "\n";
}

?>
```

Результат виконання наведеного прикладу:

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

-   [MongoDB\\BSON\\Document::fromJSON()](mongodb-bson-document.fromjson.md) \- Створює новий екземпляр документа з рядка JSON
-   [MongoDB\\BSON\\Document::toCanonicalExtendedJSON()](mongodb-bson-document.tocanonicalextendedjson.md) \- Повертає Canonical Extended JSON-подання BSON-документу
-   [MongoDB\\BSON\\toRelaxedExtendedJSON()](function.mongodb.bson-torelaxedextendedjson.md) \- Повертає Relaxed Extended JSON подання значення BSON
-   [» Специфікація Extended JSON](https://github.com/mongodb/specifications/blob/master/source/extended-json.rst)
-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
