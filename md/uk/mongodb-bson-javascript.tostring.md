Повертає код JavaScript

-   [« MongoDB\\BSON\\Javascript::serialize](mongodb-bson-javascript.serialize.html)
    
-   [MongoDB\\BSON\\Javascript::unserialize »](mongodb-bson-javascript.unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.html)
    
-   Повертає код JavaScript
    

# MongoDBBSONJavascript::toString

(mongodb >=1.2.0)

MongoDBBSONJavascript::toString — Повертає код JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::__toString(): string
```

Цей метод є псевдонімом: [MongoDB\\BSON\\Javascript::getCode()](mongodb-bson-javascript.getcode.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає JavaScript.

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONJavascript::toString()****

```php
<?php

var_dump((string) new MongoDB\BSON\Javascript('function foo(bar) { return bar; }'));

?>
```

Результат виконання цього прикладу:

```
string(33) "function foo(bar) { return bar; }"
```

### Дивіться також

-   [MongoDB\\BSON\\Javascript::getCode()](mongodb-bson-javascript.getcode.html) - Повертає код JavaScript
-   [» Типы BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)