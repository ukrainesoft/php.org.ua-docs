---
navigation:
  - mongodb-bson-utcdatetime.serialize.html: '« MongoDBBSONUTCDateTime::serialize'
  - mongodb-bson-utcdatetime.tostring.html: 'MongoDBBSONUTCDateTime::toString »'
  - index.html: PHP Manual
  - class.mongodb-bson-utcdatetime.html: MongoDBBSONUTCDateTime
title: 'MongoDBBSONUTCDateTime::toDateTime'
---
# MongoDBBSONUTCDateTime::toDateTime

(mongodb >=1.0.0)

MongoDBBSONUTCDateTime::toDateTime — Повертає уявлення DateTime цього UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::toDateTime(): DateTime
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виставу [DateTime](class.datetime.html) цього UTCDateTime. Повернутий [DateTime](class.datetime.html) буде використовувати часовий пояс UTC.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONUTCDatetime::toDateTime()****

```php
<?php

$utcdatetime = new MongoDB\BSON\UTCDateTime(1416445411987);
$datetime = $utcdatetime->toDateTime();
var_dump($datetime->format('r'));
var_dump($datetime->format('U.u'));
var_dump($datetime->getTimezone());

?>
```

Результатом виконання цього прикладу буде щось подібне:

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
