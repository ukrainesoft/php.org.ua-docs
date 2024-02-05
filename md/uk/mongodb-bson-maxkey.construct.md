---
navigation:
  - class.mongodb-bson-maxkey.md: « MongoDB\\BSON\\MaxKey
  - mongodb-bson-maxkey.jsonserialize.md: 'MongoDB\\BSON\\MaxKey::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-maxkey.md: MongoDB\\BSON\\MaxKey
title: 'MongoDB\\BSON\\MaxKey::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\MaxKey::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\MaxKey::\_\_construct — Конструктор MaxKey

### Опис

```methodsynopsis
final public MongoDB\BSON\MaxKey::__construct()
```

### Список параметрів

Ця функція не має параметрів.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\MaxKey::\_\_construct()\*\*\*\*

```php
<?php

var_dump(new MongoDB\BSON\MaxKey());

?>
```

Результат виконання наведеного прикладу:

```
object(MongoDB\BSON\MaxKey)#1 (0) {
}
```

### Дивіться також

-   [» Типи BSON](https://www.mongodb.com/docs/manual/reference/bson-types/)
