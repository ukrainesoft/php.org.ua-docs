---
navigation:
  - class.mongodb-bson-utcdatetime.md: « MongoDB\\BSON\\UTCDateTime
  - mongodb-bson-utcdatetime.jsonserialize.md: 'MongoDB\\BSON\\UTCDateTime::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetime.md: MongoDB\\BSON\\UTCDateTime
title: 'MongoDB\\BSON\\UTCDateTime::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\UTCDateTime::\_\_construct

(mongodb >=1.0.0)

MongoDB\\BSON\\UTCDateTime::\_\_construct — Створює новий UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::__construct(int|float|string|DateTimeInterface|null $milliseconds = null)
```

### Список параметрів

`milliseconds`(int|float|string|[DateTimeInterface](class.datetimeinterface.md)|null)

Кількість мілісекунд з часів Unix (1 січня 1970). Негативні значення становлять дати до 1970 року. Це значення може бути представлене як 64-розрядний int. Для сумісності в 32-бітових системах цей параметр також може бути представлений як float або string.

Якщо аргумент є [DateTimeInterface](class.datetimeinterface.md), З цього значення буде отримано кількість мілісекунд, що пройшли з початку епохи Unix.

Якщо цей аргумент дорівнює **`null`**, буде використовуватись поточний час за промовчанням.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.2.0 |  |
| Аргумент`milliseconds` є необов'язковим і за умовчанням дорівнює **`null`** (Тобто поточний час). Аргумент також приймає [DateTimeInterface](class.datetimeinterface.md)який може використовуватися для отримання кількості мілісекунд з початку епохи Unix. Раніше приймався лише тип int, float чи string. |  |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\BSON\\UTCDateTime::\_\_construct()\*\*\*\*

```php
<?php

var_dump(new MongoDB\BSON\UTCDateTime);

var_dump(new MongoDB\BSON\UTCDateTime(new DateTime));

var_dump(new MongoDB\BSON\UTCDateTime(1416445411987));

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\BSON\UTCDateTime)#1 (1) {
  ["milliseconds"]=>
  string(13) "1484852905560"
}
object(MongoDB\BSON\UTCDateTime)#1 (1) {
  ["milliseconds"]=>
  string(13) "1484852905560"
}
object(MongoDB\BSON\UTCDateTime)#1 (1) {
  ["milliseconds"]=>
  string(13) "1416445411987"
}
```

### Дивіться також

-   [» Типи BSON: Date](https://www.mongodb.com/docs/manual/reference/bson-types/#date)
