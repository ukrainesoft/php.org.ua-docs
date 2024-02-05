---
navigation:
  - class.mongodb-bson-javascript.md: « MongoDB\\BSON\\Javascript
  - mongodb-bson-javascript.getcode.md: 'MongoDB\\BSON\\Javascript::getCode »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\Javascript::\_\_construct - конструктор Javascript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::__construct(string $code, array|object|null $scope = null)
```

### Список параметрів

`code`(string)

Код Javascript.

`scope`(array|object)

Контекст Javascript.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Породжує виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо `code`містить null-байти.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.2.0 |  |
| Породжує виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо `code` містить null-байти. Раніше, в такому випадку, аргумент обрізався про першого null-байту, що зустрівся. |  |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Javascript::\_\_construct()\*\*\*\*

```php
<?php

$code = new MongoDB\BSON\Javascript('function() { return 1; }');
var_dump($code);

$codews = new MongoDB\BSON\Javascript('function() { return foo; }', ['foo' => 'bar']);
var_dump($codews);

?>
```

Результат виконання наведеного прикладу:

```
object(MongoDB\BSON\Javascript)#1 (2) {
  ["javascript"]=>
  string(24) "function() { return 1; }"
  ["scope"]=>
  object(stdClass)#2 (0) {
  }
}
object(MongoDB\BSON\Javascript)#2 (2) {
  ["javascript"]=>
  string(26) "function() { return foo; }"
  ["scope"]=>
  object(stdClass)#1 (1) {
    ["foo"]=>
    string(3) "bar"
  }
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
