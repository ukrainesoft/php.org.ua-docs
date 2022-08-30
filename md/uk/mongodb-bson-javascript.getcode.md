Повертає код JavaScript

-   [« MongoDBBSONJavascript::construct](mongodb-bson-javascript.construct.html)
    
-   [MongoDBBSONJavascript::getScope »](mongodb-bson-javascript.getscope.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONJavascript](class.mongodb-bson-javascript.html)
    
-   Повертає код JavaScript
    

# MongoDBBSONJavascript::getCode

(mongodb >=1.2.0)

MongoDBBSONJavascript::getCode — Повертає код JavaScript

### Опис

```methodsynopsis
final public MongoDB\BSON\Javascript::getCode(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає JavaScript.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONJavascript::getCode()****

```php
<?php

$js = new MongoDB\BSON\Javascript('function foo(bar) { return bar; }');
var_dump($js->getCode());

?>
```

Результат виконання цього прикладу:

```
string(33) "function foo(bar) { return bar; }"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)