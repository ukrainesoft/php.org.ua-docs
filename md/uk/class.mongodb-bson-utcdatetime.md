---
navigation:
  - mongodb-bson-timestamp.unserialize.md: '« MongoDBBSONTimestamp::unserialize'
  - mongodb-bson-utcdatetime.construct.md: 'MongoDBBSONUTCDateTime::construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Клас MongoDBBSONUTCDateTime
---
# Клас MongoDBBSONUTCDateTime

(mongodb >=1.0.0)

## Вступ

Уявляє [» дату BSON](https://www.mongodb.com/docs/manual/reference/bson-types/#date). Значення є 64-розрядним цілим числом, що представляє кількість мілісекунд з початку епохи Unix (1 січня 1970 р.). Негативні значення становлять дати до 1970 року.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\UTCDateTime
     

     implements 
       MongoDB\BSON\UTCDateTimeInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {


    /* Методы */
    
   final public __construct(int|float|string|DateTimeInterface|null $milliseconds = null)
final public jsonSerialize(): mixed
final public serialize(): string
final public toDateTime(): DateTime
final public __toString(): string
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDBBSONUTCDateTimeInterface](class.mongodb-bson-utcdatetimeinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDBBSONUTCDateTime::construct](mongodb-bson-utcdatetime.construct.md) — Створює новий UTCDateTime
-   [MongoDBBSONUTCDateTime::jsonSerialize](mongodb-bson-utcdatetime.jsonserialize.md) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONUTCDateTime::serialize](mongodb-bson-utcdatetime.serialize.md) - Серіалізує UTCDateTime
-   [MongoDBBSONUTCDateTime::toDateTime](mongodb-bson-utcdatetime.todatetime.md) — Повертає уявлення DateTime цього UTCDateTime
-   [MongoDBBSONUTCDateTime::toString](mongodb-bson-utcdatetime.tostring.md) — Повертає рядкову виставу UTCDateTime
-   [MongoDBBSONUTCDateTime::unserialize](mongodb-bson-utcdatetime.unserialize.md) - Десеріалізує UTCDateTime
