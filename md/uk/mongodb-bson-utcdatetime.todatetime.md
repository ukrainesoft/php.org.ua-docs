---
navigation:
  - mongodb-bson-utcdatetime.serialize.md: '« MongoDB\\BSON\\UTCDateTime::serialize'
  - mongodb-bson-utcdatetime.tostring.md: 'MongoDB\\BSON\\UTCDateTime::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime
title: 'MongoDB\\BSON\\UTCDateTime::toDateTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\UTCDateTime::toDateTime

(mongodb >=1.0.0)

MongoDB\\BSON\\UTCDateTime::toDateTime — Повертає уявлення DateTime цього UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::toDateTime(): DateTime
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает представление[DateTime](class.datetime.md) цього UTCDateTime. Повернутий [DateTime](class.datetime.md) буде використовувати часовий пояс UTC.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\UTCDatetime::toDateTime()\*\*\*\*

```php
<?php

$utcdatetime = new MongoDB\BSON\UTCDateTime(1416445411987);
$datetime = $utcdatetime->toDateTime();
var_dump($datetime->format('r'));
var_dump($datetime->format('U.u'));
var_dump($datetime->getTimezone());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(31) "Thu, 20 Nov 2014 01:03:31 +0000"
string(17) "1416445411.987000"
object(DateTimeZone)#3 (2) {
  ["timezone_type"]=>
  int(1)
  ["timezone"]=>
  string(6) "+00:00"
}
```

### Дивіться також

-   [» Типи BSON: Date](https://www.mongodb.com/docs/manual/reference/bson-types/#date)
