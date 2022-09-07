---
navigation:
  - mongodb-bson-javascript.getcode.md: '« MongoDBBSONJavascript::getCode'
  - mongodb-bson-javascript.jsonserialize.md: 'MongoDBBSONJavascript::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDBBSONJavascript
title: 'MongoDBBSONJavascript::getScope'
---
# MongoDBBSONJavascript::getScope

(mongodb >=1.2.0)

MongoDBBSONJavascript::getScope — Повертає область документа JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::getScope(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає область документа JavaScript або **`null`** якщо області немає.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONJavascript::getScope()****

```php
<?php

$js = new MongoDB\BSON\Javascript('function foo(bar) { return bar; }');
var_dump($js->getScope());

$js = new MongoDB\BSON\Javascript('function foo() { return foo; }', ['foo' => 42]);
var_dump($js->getScope());

?>
```

Результат виконання цього прикладу:

```
NULL
object(stdClass)#1 (1) {
  ["foo"]=>
  int(42)
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
