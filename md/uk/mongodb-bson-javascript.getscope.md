---
navigation:
  - mongodb-bson-javascript.getcode.md: '« MongoDB\\BSON\\Javascript::getCode'
  - mongodb-bson-javascript.jsonserialize.md: 'MongoDB\\BSON\\Javascript::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::getScope'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::getScope

(mongodb >=1.2.0)

MongoDB\\BSON\\Javascript::getScope — Повертає область документа JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::getScope(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає область документа JavaScript або **`null`** якщо області немає.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Javascript::getScope()\*\*\*\*

```php
<?php

$js = new MongoDB\BSON\Javascript('function foo(bar) { return bar; }');
var_dump($js->getScope());

$js = new MongoDB\BSON\Javascript('function foo() { return foo; }', ['foo' => 42]);
var_dump($js->getScope());

?>
```

Результат виконання наведеного прикладу:

```
NULL
object(stdClass)#1 (1) {
  ["foo"]=>
  int(42)
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
