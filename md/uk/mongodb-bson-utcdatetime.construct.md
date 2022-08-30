Створює новий UTCDateTime

-   [« MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html)
    
-   [MongoDBBSONUTCDateTime::jsonSerialize »](mongodb-bson-utcdatetime.jsonserialize.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html)
    
-   Створює новий UTCDateTime
    

# MongoDBBSONUTCDateTime::construct

(mongodb >=1.0.0)

MongoDBBSONUTCDateTime::construct — Створює новий UTCDateTime

### Опис

```methodsynopsis
final public MongoDB\BSON\UTCDateTime::__construct(int|float|string|DateTimeInterface|null $milliseconds = null)
```

### Список параметрів

`milliseconds` (int | float | string |[DateTimeInterface](class.datetimeinterface.md)|null)

Кількість мілісекунд з часів Unix (1 січня 1970). Негативні значення становлять дати до 1970 року. Це значення може бути представлене як 64-розрядний int. Для сумісності в 32-бітових системах цей параметр також може бути представлений як float або string.

Якщо аргумент є [DateTimeInterface](class.datetimeinterface.md), З цього значення буде отримано кількість мілісекунд, що пройшли з початку епохи Unix. Зверніть увагу, що у версіях PHP до 7.1.0 об'єкти [DateTime](class.datetime.md) і [DateTimeImmutable](class.datetimeimmutable.md), побудовані за поточним часом, [не включають точність менше секунди](migration71.incompatible.html#migration71.incompatible.datetime-microseconds)

Якщо цей аргумент дорівнює **`null`**, використовуватиметься поточний час за промовчанням.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.2.0 |  |
| Аргумент `milliseconds` є необов'язковим і за умовчанням дорівнює **`null`** (Тобто поточний час). Аргумент також приймає [DateTimeInterface](class.datetimeinterface.md)який може використовуватися для отримання кількості мілісекунд з початку епохи Unix. Раніше приймався лише тип int, float чи string. |  |

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONUTCDateTime::construct()****

```php
<?php

var_dump(new MongoDB\BSON\UTCDateTime);

var_dump(new MongoDB\BSON\UTCDateTime(new DateTime));

var_dump(new MongoDB\BSON\UTCDateTime(1416445411987));

?>
```

Результатом виконання цього прикладу буде щось подібне:

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