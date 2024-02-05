---
navigation:
  - mongodb-bson-objectid.construct.md: '« MongoDB\\BSON\\ObjectId::\_\_construct'
  - mongodb-bson-objectid.jsonserialize.md: 'MongoDB\\BSON\\ObjectId::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-objectid.md: MongoDB\\BSON\\ObjectId
title: 'MongoDB\\BSON\\ObjectId::getTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\ObjectId::getTimestamp

(mongodb >=1.2.0)

MongoDB\\BSON\\ObjectId::getTimestamp — Повертає позначку часу ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::getTimestamp(): int
```

Компонент мітки часу в ObjectId – це його найбільш значущі 32 біти, які позначають кількість секунд від початку епохи Unix. Це значення читається як 32-розрядне ціле число без знака з порядком байтів у старшому порядку.

> **Зауваження**: Оскільки цілий тип PHP є знаковим, деякі значення, отримані за допомогою цього методу, можуть перетворитися на негативні цілі числа на 32-бітових платформах. Для отримання строкового представлення беззнакового цілого можна скористатися шаблоном форматування %u функції [sprintf()](function.sprintf.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає позначку часу ObjectId.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Пример #1 Пример использования**MongoDB\\BSON\\ObjectId::getTimestamp()\*\*\*\*

```php
<?php

var_dump((new MongoDB\BSON\ObjectId())->getTimestamp());

var_dump((new MongoDB\BSON\ObjectId('0000002a0000000000000000'))->getTimestamp());

?>
```

Висновок наведеного прикладу буде схожим на:

```
integer(1484854719)
integer(42)
```

### Дивіться також

-   [» Довідка по ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
-   [» Типи BSON: ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
