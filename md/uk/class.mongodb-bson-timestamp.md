---
navigation:
  - mongodb-bson-regex.unserialize.md: '« MongoDB\\BSON\\Regex::unserialize'
  - mongodb-bson-timestamp.construct.md: 'MongoDB\\BSON\\Timestamp::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Timestamp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Timestamp

(mongodb >=1.0.0)

## Вступ

Представляет[»¦мітку часу BSON](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps). Значення складається з 4-байтової мітки часу (тобто секунди з початку епохи) та 4-байтового збільшення.

> **Зауваження**: Це внутрішній тип MongoDB, що використовується для реплікації та поділу. Він не призначений для загального зберігання дат (замість нього слід використовувати [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.md)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\Timestamp
     

     implements 
       MongoDB\BSON\TimestampInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {


    /* Методы */
    
   final public __construct(int $increment, int $timestamp)
final public getIncrement(): int
final public getTimestamp(): int
final public jsonSerialize(): mixed
final public serialize(): string
final public __toString(): string
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\TimestampInterface](class.mongodb-bson-timestampinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\Timestamp::\_\_construct](mongodb-bson-timestamp.construct.md) \- Створює новий Timestamp
-   [MongoDB\\BSON\\Timestamp::getIncrement](mongodb-bson-timestamp.getincrement.md)— Повертає компонент збільшення Timestamp
-   [MongoDB\\BSON\\Timestamp::getTimestamp](mongodb-bson-timestamp.gettimestamp.md) \- Повертає компонент позначки часу Timestamp
-   [MongoDB\\BSON\\Timestamp::jsonSerialize](mongodb-bson-timestamp.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Timestamp::serialize](mongodb-bson-timestamp.serialize.md) \- Серіалізує Timestamp
-   [MongoDB\\BSON\\Timestamp::\_\_function toString() { \[native code\] }](mongodb-bson-timestamp.tostring.md)— Повертає строкову виставу Timestamp
-   [MongoDB\\BSON\\Timestamp::unserialize](mongodb-bson-timestamp.unserialize.md) \- Десеріалізує Timestamp
