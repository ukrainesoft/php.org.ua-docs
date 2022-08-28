Інтерфейс MongoDBBSONUTCDateTimeInterface

-   [« MongoDB\\BSON\\TimestampInterface::\_\_toString](mongodb-bson-timestampinterface.tostring.html)
    
-   [MongoDB\\BSON\\UTCDateTimeInterface::toDateTime »](mongodb-bson-utcdatetimeinterface.todatetime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Інтерфейс MongoDBBSONUTCDateTimeInterface
    

# Інтерфейс MongoDBBSONUTCDateTimeInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.html), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\UTCDateTimeInterface
     
     {
    /* Методы */
    
   abstract public toDateTime(): DateTime
abstract public __toString(): string

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\UTCDateTimeInterface::toDateTime](mongodb-bson-utcdatetimeinterface.todatetime.html) — Повертає уявлення DateTime цього UTCDateTimeInterface
-   [MongoDB\\BSON\\UTCDateTimeInterface::\_\_toString](mongodb-bson-utcdatetimeinterface.tostring.html) — Повертає рядкову виставу UTCDateTimeInterface