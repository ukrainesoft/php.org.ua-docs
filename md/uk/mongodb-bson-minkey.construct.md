---
navigation:
  - class.mongodb-bson-minkey.md: « MongoDB\\BSON\\MinKey
  - mongodb-bson-minkey.jsonserialize.md: 'MongoDB\\BSON\\MinKey::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-minkey.md: MongoDB\\BSON\\MinKey
title: 'MongoDB\\BSON\\MinKey::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\MinKey::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\MinKey::\_\_construct — Конструктор MinKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MinKey::__construct()
```

### Список параметрів

Ця функція не має параметрів.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\MinKey::\_\_construct()\*\*\*\*

```php
<?php

var_dump(new MongoDB\BSON\MinKey());

?>
```

Результат виконання наведеного прикладу:

```
object(MongoDB\BSON\MinKey)#1 (0) {
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
