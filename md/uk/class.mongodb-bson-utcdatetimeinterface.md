---
navigation:
  - mongodb-bson-timestampinterface.tostring.md: >-
      « MongoDB\\BSON\\TimestampInterface::\_\_function toString() { [native
      code] }
  - mongodb-bson-utcdatetimeinterface.todatetime.md: 'MongoDB\\BSON\\UTCDateTimeInterface::toDateTime »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\UTCDateTimeInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\UTCDateTimeInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\UTCDateTimeInterface::toDateTime](mongodb-bson-utcdatetimeinterface.todatetime.md)— Повертає уявлення DateTime цього UTCDateTimeInterface
-   [MongoDB\\BSON\\UTCDateTimeInterface::\_\_function toString() { \[native code\] }](mongodb-bson-utcdatetimeinterface.tostring.md)— Повертає рядкову виставу UTCDateTimeInterface
