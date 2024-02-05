---
navigation:
  - mongodb-bson-regex.construct.md: '« MongoDB\\BSON\\Regex::\_\_construct'
  - mongodb-bson-regex.getpattern.md: 'MongoDB\\BSON\\Regex::getPattern »'
  - index.md: PHP Manual
  - class.mongodb-bson-regex.md: MongoDB\\BSON\\Regex
title: 'MongoDB\\BSON\\Regex::getFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Regex::getFlags

(mongodb >=1.0.0)

MongoDB\\BSON\\Regex::getFlags — Повертає прапори Regex

### Опис

```methodsynopsis
final public MongoDB\BSON\Regex::getFlags(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає прапори Regex.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Regex::getFlags()\*\*\*\*

```php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump($regex->getFlags());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "i"
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
-   [» Підтримувані прапори регулярних виразів](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)
