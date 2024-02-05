---
navigation:
  - class.mongodb-bson-timestamp.md: « MongoDB\\BSON\\Timestamp
  - mongodb-bson-timestamp.getincrement.md: 'MongoDB\\BSON\\Timestamp::getIncrement »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.md: MongoDB\\BSON\\Timestamp
title: 'MongoDB\\BSON\\Timestamp::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Timestamp::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\Timestamp::\_\_construct - Створює новий Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::__construct(int $increment, int $timestamp)
```

### Список параметрів

`increment`(int)

32-розрядне ціле число, що означає порядковий номер, що збільшується, для операцій протягом цієї секунди.

`timestamp`(int)

32-розрядне ціле число, що означає секунди з початку епохи Unix.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\Timestamp::\_\_construct()\*\*\*\*

```php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);

?>
```

Результат виконання наведеного прикладу:

```
object(MongoDB\BSON\Timestamp)#1 (2) {
  ["increment"]=>
  int(1234)
  ["timestamp"]=>
  int(5678)
}
```

### Дивіться також

-   [» Типи BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)
