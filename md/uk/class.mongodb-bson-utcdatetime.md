---
navigation:
  - mongodb-bson-timestamp.unserialize.md: '« MongoDB\\BSON\\Timestamp::unserialize'
  - mongodb-bson-utcdatetime.construct.md: 'MongoDB\\BSON\\UTCDateTime::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\UTCDateTime
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\UTCDateTime

(mongodb >=1.0.0)

## Вступ

Представляет[» дату BSON](https://www.mongodb.com/docs/manual/reference/bson-types/#date). Значення є 64-розрядним цілим числом, що представляє кількість мілісекунд з початку епохи Unix (1 січня 1970 р.). Негативні значення становлять дати до 1970 року.

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
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\UTCDateTimeInterface](class.mongodb-bson-utcdatetimeinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\UTCDateTime::\_\_construct](mongodb-bson-utcdatetime.construct.md)— Створює новий UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::jsonSerialize](mongodb-bson-utcdatetime.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\UTCDateTime::serialize](mongodb-bson-utcdatetime.serialize.md) \- Серіалізує UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::toDateTime](mongodb-bson-utcdatetime.todatetime.md)— Повертає уявлення DateTime цього UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::\_\_function toString() { \[native code\] }](mongodb-bson-utcdatetime.tostring.md)— Повертає рядкову виставу UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::unserialize](mongodb-bson-utcdatetime.unserialize.md) \- Десеріалізує UTCDateTime
