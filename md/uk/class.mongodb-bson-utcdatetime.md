Клас MongoDBBSONUTCDateTime

-   [« MongoDB\\BSON\\Timestamp::unserialize](mongodb-bson-timestamp.unserialize.html)
    
-   [MongoDB\\BSON\\UTCDateTime::\_\_construct »](mongodb-bson-utcdatetime.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Клас MongoDBBSONUTCDateTime
    

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

| Версия              | Описание                                                                                                      |
|---------------------|---------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+.                                          |
| PECL mongodb 1.3.0  | Реалізує інтерфейс [MongoDB\\BSON\\UTCDateTimeInterface](class.mongodb-bson-utcdatetimeinterface.html)        |
| PECL mongodb 1.2.0  | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDB\\BSON\\UTCDateTime::\_\_construct](mongodb-bson-utcdatetime.construct.html) — Створює новий UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::jsonSerialize](mongodb-bson-utcdatetime.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\UTCDateTime::serialize](mongodb-bson-utcdatetime.serialize.html) - Серіалізує UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::toDateTime](mongodb-bson-utcdatetime.todatetime.html) — Повертає уявлення DateTime цього UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::\_\_toString](mongodb-bson-utcdatetime.tostring.html) — Повертає рядкову виставу UTCDateTime
-   [MongoDB\\BSON\\UTCDateTime::unserialize](mongodb-bson-utcdatetime.unserialize.html) - Десеріалізує UTCDateTime