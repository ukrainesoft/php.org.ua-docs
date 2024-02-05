---
navigation:
  - ref.bson.functions.md: « Функції
  - function.mongodb.bson-fromphp.md: MongoDB\\BSON\\fromPHP »
  - index.md: PHP Manual
  - ref.bson.functions.md: Функції
title: MongoDB\\BSON\\fromJSON
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\fromJSON

(mongodb >=1.0.0)

MongoDB\\BSON\\fromJSON — Повертає подання BSON значення JSON

### Опис

```methodsynopsis
MongoDB\BSON\fromJSON(string $json): string
```

Перетворює рядок [» Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/) у її уявлення BSON.

### Список параметрів

`json`(string)

Значення JSON для перетворення.

### Значення, що повертаються

Повертає серіалізований документ BSON у вигляді двійкового рядка.

### Помилки

-   Видає[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md), якщо значення JSON не може бути перетворене на BSON (наприклад, через синтаксичну помилку).

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\fromJSON()\*\*\*\*

```php
<?php

$json = '{ "_id": { "$oid": "563143b280d2387c91807965" } }';
$bson = MongoDB\BSON\fromJSON($json);
$value = MongoDB\BSON\toPHP($bson);
var_dump($value);

?>
```

Результат виконання наведеного прикладу:

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

-   [MongoDB\\BSON\\Document::fromJSON()](mongodb-bson-document.fromjson.md) \- Створює новий екземпляр документа з рядка JSON
-   [MongoDB\\BSON\\toJSON()](function.mongodb.bson-tojson.md) \- Повертає Legacy Extended JSON-подання значення BSON
-   [» MongoDB Extended JSON](https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/)
-   [» MongoDB BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
