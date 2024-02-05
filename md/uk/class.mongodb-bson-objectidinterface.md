---
navigation:
  - class.mongodb-bson-minkeyinterface.md: « MongoDB\\BSON\\MinKeyInterface
  - mongodb-bson-objectidinterface.gettimestamp.md: 'MongoDB\\BSON\\ObjectIdInterface::getTimestamp »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\ObjectIdInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\ObjectIdInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md), але також може бути використаний як параметр, повертається значення або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\ObjectIdInterface
     
     {
    /* Методы */
    
   abstract public getTimestamp(): int
abstract public __toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\ObjectIdInterface::getTimestamp](mongodb-bson-objectidinterface.gettimestamp.md)— Повертає компонент позначки часу ObjectIdInterface
-   [MongoDB\\BSON\\ObjectIdInterface::\_\_function toString() { \[native code\] }](mongodb-bson-objectidinterface.tostring.md)— Повертає шістнадцяткову виставу ObjectIdInterface
