---
navigation:
  - mongodb-bson-timestampinterface.tostring.md: '« MongoDBBSONTimestampInterface::toString'
  - mongodb-bson-utcdatetimeinterface.todatetime.md: 'MongoDBBSONUTCDateTimeInterface::toDateTime »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Інтерфейс MongoDBBSONUTCDateTimeInterface
---
# Інтерфейс MongoDBBSONUTCDateTimeInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

-   [MongoDBBSONUTCDateTimeInterface::toDateTime](mongodb-bson-utcdatetimeinterface.todatetime.md) — Повертає уявлення DateTime цього UTCDateTimeInterface
-   [MongoDBBSONUTCDateTimeInterface::toString](mongodb-bson-utcdatetimeinterface.tostring.md) — Повертає рядкову виставу UTCDateTimeInterface
