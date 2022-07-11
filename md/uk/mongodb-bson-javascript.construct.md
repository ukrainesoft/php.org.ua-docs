- [« MongoDB \ BSON \ Javascript](class.mongodb-bson-javascript.md)
- [MongoDB\BSON\Javascript::getCode »](mongodb-bson-javascript.getcode.md)

- [PHP Manual](index.md)
- [MongoDB\BSON\Javascript](class.mongodb-bson-javascript.md)
- Конструктор Javascript

# MongoDB\BSON\Javascript::\_\_construct

(mongodb \>=1.0.0)

MongoDB\BSON\Javascript::\_\_construct - Конструктор Javascript

### Опис

final public **MongoDB\BSON\Javascript::\_\_construct**(string `$code`,
array\|object `$scope` = ?)

### Список параметрів

`code` (string)
Код Javascript.

`scope` (array\|object)
Контекст Javascript.

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).
- породжує виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
якщо `code` містить null-байти.

### Список змін

| Версія             | Опис                                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.2.0 | Породжує виняток [MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо code містить null-байти. Раніше, в такому випадку, аргумент обрізався для першого null-байту, що зустрівся. |

### Приклади

**Приклад #1 Приклад використання
**MongoDB\BSON\Javascript::\_\_construct()****

` <?php$code = new MongoDB\BSON\Javascript('function() { return 1; }');var_dump($code);$codews = new MongoDB\BSON\Javascript('function()n| }', ['foo' => 'bar']);var_dump($codews);?> `

Результат виконання цього прикладу:

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

### Дивіться також

- [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
