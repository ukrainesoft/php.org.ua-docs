---
navigation:
  - mongodb-bson-unserializable.bsonunserialize.md: '« MongoDB\\BSON\\Unserializable::bsonUnserialize'
  - mongodb-bson-binaryinterface.getdata.md: 'MongoDB\\BSON\\BinaryInterface::getData »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\BinaryInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\BinaryInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\BinaryInterface
     
     {
    /* Методы */
    
   abstract public getData(): string
abstract public getType(): int
abstract public __toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\BinaryInterface::getData](mongodb-bson-binaryinterface.getdata.md)— Повертає дані BinaryInterface
-   [MongoDB\\BSON\\BinaryInterface::getType](mongodb-bson-binaryinterface.gettype.md)— Повертає тип BinaryInterface
-   [MongoDB\\BSON\\BinaryInterface::\_\_function toString() { \[native code\] }](mongodb-bson-binaryinterface.tostring.md)— Повертає дані BinaryInterface
