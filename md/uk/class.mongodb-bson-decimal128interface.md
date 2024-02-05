---
navigation:
  - mongodb-bson-binaryinterface.tostring.md: >-
      « MongoDB\\BSON\\BinaryInterface::\_\_function toString() { [native code]
      }
  - mongodb-bson-decimal128interface.tostring.md: 'MongoDB\\BSON\\Decimal128Interface::\_\_toString »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\Decimal128Interface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\Decimal128Interface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\Decimal128Interface
     
     {
    /* Методы */
    
   abstract public __toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\Decimal128Interface::\_\_function toString() { \[native code\] }](mongodb-bson-decimal128interface.tostring.md)— Повертає рядкову виставу Decimal128Interface
