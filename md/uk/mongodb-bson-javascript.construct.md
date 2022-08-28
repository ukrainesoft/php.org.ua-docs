Конструктор Javascript

-   [« MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.html)
    
-   [MongoDB\\BSON\\Javascript::getCode »](mongodb-bson-javascript.getcode.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.html)
    
-   Конструктор Javascript
    

# MongoDBBSONJavascript::construct

(mongodb >=1.0.0)

MongoDBBSONJavascript::construct - конструктор Javascript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::__construct(string $code, array|object|null $scope = null)
```

### Список параметрів

`code` (string)

Код Javascript.

`scope` (array | об'єкт)

Контекст Javascript.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Породжує виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) якщо `code` містить null-байти.

### список змін

| Версия                                                                                                                                                                                                                                                   | Описание |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| PECL mongodb 1.2.0                                                                                                                                                                                                                                       |          |
| Породжує виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) якщо `code` містить null-байти. Раніше, в такому випадку, аргумент обрізався про першого null-байту, що зустрівся. |          |

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONJavascript::construct()****

```php
<?php

$code = new MongoDB\BSON\Javascript('function() { return 1; }');
var_dump($code);

$codews = new MongoDB\BSON\Javascript('function() { return foo; }', ['foo' => 'bar']);
var_dump($codews);

?>
```

Результат виконання цього прикладу:

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

-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)