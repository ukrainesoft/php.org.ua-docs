Клас MongoDBBSONTimestamp

-   [« MongoDBBSONRegex::unserialize](mongodb-bson-regex.unserialize.html)
    
-   [MongoDBBSONTimestamp::construct »](mongodb-bson-timestamp.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSON](book.bson.html)
    
-   Клас MongoDBBSONTimestamp
    

# Клас MongoDBBSONTimestamp

(mongodb >=1.0.0)

## Вступ

Уявляє [» метку времени BSON](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps). Значення складається з 4-байтової мітки часу (тобто секунди з початку епохи) та 4-байтового збільшення.

> **Зауваження**: Це внутрішній тип MongoDB, що використовується для реплікації та поділу. Він не призначений для загального зберігання дат (замість нього слід використовувати [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html)

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
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия              | Описание                                                                                                      |
|---------------------|---------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+.                                          |
| PECL mongodb 1.3.0  | Реалізує інтерфейс [MongoDBBSONTimestampInterface](class.mongodb-bson-timestampinterface.html)                |
| PECL mongodb 1.2.0  | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDBBSONTimestamp::construct](mongodb-bson-timestamp.construct.html) - Створює новий Timestamp
-   [MongoDBBSONTimestamp::getIncrement](mongodb-bson-timestamp.getincrement.html) — Повертає компонент збільшення Timestamp
-   [MongoDBBSONTimestamp::getTimestamp](mongodb-bson-timestamp.gettimestamp.html) - Повертає компонент позначки часу Timestamp
-   [MongoDBBSONTimestamp::jsonSerialize](mongodb-bson-timestamp.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONTimestamp::serialize](mongodb-bson-timestamp.serialize.html) - Серіалізує Timestamp
-   [MongoDBBSONTimestamp::toString](mongodb-bson-timestamp.tostring.html) — Повертає строкову виставу Timestamp
-   [MongoDBBSONTimestamp::unserialize](mongodb-bson-timestamp.unserialize.html) - Десеріалізує Timestamp