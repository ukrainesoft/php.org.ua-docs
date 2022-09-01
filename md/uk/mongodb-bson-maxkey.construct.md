---
navigation:
  - class.mongodb-bson-maxkey.html: « MongoDBBSONMaxKey
  - mongodb-bson-maxkey.jsonserialize.html: 'MongoDBBSONMaxKey::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-maxkey.html: MongoDBBSONMaxKey
title: 'MongoDBBSONMaxKey::construct'
---
# MongoDBBSONMaxKey::construct

(mongodb >=1.0.0)

MongoDBBSONMaxKey::construct — Конструктор MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::__construct()
```

### Список параметрів

Ця функція не має параметрів.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONMaxKey::construct()****

```php
<?php

var_dump(new MongoDB\BSON\MaxKey());

?>
```

Результат виконання цього прикладу:

```
object(MongoDB\BSON\MaxKey)#1 (0) {
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
