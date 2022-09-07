---
navigation:
  - class.mongodb-bson-utcdatetimeinterface.md: « MongoDBBSONUTCDateTimeInterface
  - mongodb-bson-utcdatetimeinterface.tostring.md: 'MongoDBBSONUTCDateTimeInterface::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-utcdatetimeinterface.md: MongoDBBSONUTCDateTimeInterface
title: 'MongoDBBSONUTCDateTimeInterface::toDateTime'
---
# MongoDBBSONUTCDateTimeInterface::toDateTime

(mongodb >=1.3.0)

MongoDBBSONUTCDateTimeInterface::toDateTime — Повертає уявлення DateTime цього UTCDateTimeInterface

### Опис

```methodsynopsis
abstract public MongoDB\BSON\UTCDateTimeInterface::toDateTime(): DateTime
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виставу [DateTime](class.datetime.md) цього UTCDateTimeInterface. Повернутий [DateTime](class.datetime.md) повинен використовувати часовий пояс UTC.

### Дивіться також

-   [MongoDBBSONUTCDateTime::toDateTime()](mongodb-bson-utcdatetime.todatetime.md) - Повертає уявлення DateTime цього UTCDateTime
