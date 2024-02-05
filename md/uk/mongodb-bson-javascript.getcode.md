---
navigation:
  - mongodb-bson-javascript.construct.md: '« MongoDB\\BSON\\Javascript::\_\_construct'
  - mongodb-bson-javascript.getscope.md: 'MongoDB\\BSON\\Javascript::getScope »'
  - index.md: PHP Manual
  - class.mongodb-bson-javascript.md: MongoDB\\BSON\\Javascript
title: 'MongoDB\\BSON\\Javascript::getCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Javascript::getCode

(mongodb >=1.2.0)

MongoDB\\BSON\\Javascript::getCode — Повертає код JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::getCode(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає JavaScript.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\Javascript::getCode()\*\*\*\*

```php
<?php

$js = new MongoDB\BSON\Javascript('function foo(bar) { return bar; }');
var_dump($js->getCode());

?>
```

Результат виконання наведеного прикладу:

```
string(33) "function foo(bar) { return bar; }"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
