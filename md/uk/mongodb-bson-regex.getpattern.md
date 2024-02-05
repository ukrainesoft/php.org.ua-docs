---
navigation:
  - mongodb-bson-regex.getflags.md: '« MongoDB\\BSON\\Regex::getFlags'
  - mongodb-bson-regex.jsonserialize.md: 'MongoDB\\BSON\\Regex::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex
title: 'MongoDB\\BSON\\Regex::getPattern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Regex::getPattern

(mongodb >=1.0.0)

MongoDB\\BSON\\Regex::getPattern — Повертає шаблон Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::getPattern(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шаблон Regex.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Regex::getPattern()\*\*\*\*

```php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump($regex->getPattern());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "regex"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
