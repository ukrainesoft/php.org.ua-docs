---
navigation:
  - ref.bson.functions.md: « Функції
  - function.mongodb.bson-fromphp.md: MongoDBBSONfromPHP »
  - index.md: PHP Manual
  - ref.bson.functions.md: Функції
title: MongoDBBSONfromJSON
---
# MongoDBBSONfromJSON

(mongodb >=1.0.0)

MongoDBBSONfromJSON — Повертає подання BSON значення JSON

### Опис

```methodsynopsis
MongoDB\BSON\fromJSON(string $json): string
```

Перетворює рядок [» Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/) у її уявлення BSON.

### Список параметрів

`json` (string)

Значення JSON для перетворення.

### Значення, що повертаються

Серіалізований документ BSON у вигляді двійкового рядка.

### Помилки

-   Видає [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), якщо значення JSON не може бути перетворено на BSON (наприклад, через синтаксичну помилку).

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONfromJSON()****

```php
<?php

$json = '{ "_id": { "$oid": "563143b280d2387c91807965" } }';
$bson = MongoDB\BSON\fromJSON($json);
$value = MongoDB\BSON\toPHP($bson);
var_dump($value);

?>
```

Результат виконання цього прикладу:

```
object(stdClass)#2 (1) {
  ["_id"]=>
  object(MongoDB\BSON\ObjectId)#1 (1) {
    ["oid"]=>
    string(24) "563143b280d2387c91807965"
  }
}
```

### Дивіться також

-   [MongoDBBSONtoJSON()](function.mongodb.bson-tojson.md) - Повертає Legacy Extended JSON подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
