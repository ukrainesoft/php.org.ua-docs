---
navigation:
  - mongodb-bson-binaryinterface.tostring.md: '« MongoDBBSONBinaryInterface::toString'
  - mongodb-bson-decimal128interface.tostring.md: 'MongoDBBSONDecimal128Interface::toString »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Інтерфейс MongoDBBSONDecimal128Interface
---
# Інтерфейс MongoDBBSONDecimal128Interface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\Decimal128Interface
     
     {
    /* Методы */
    
   abstract public __toString(): string

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONDecimal128Interface::toString](mongodb-bson-decimal128interface.tostring.md) — Повертає рядкову виставу Decimal128Interface
