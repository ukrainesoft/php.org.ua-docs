---
navigation:
  - mongodb-bson-regexinterface.tostring.md: '« MongoDBBSONRegexInterface::toString'
  - mongodb-bson-timestampinterface.getincrement.md: 'MongoDBBSONTimestampInterface::getIncrement »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Інтерфейс MongoDBBSONTimestampInterface
---
# Інтерфейс MongoDBBSONTimestampInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\TimestampInterface
     
     {
    /* Методы */
    
   abstract public getIncrement(): int
abstract public getTimestamp(): int
abstract public __toString(): string

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONTimestampInterface::getIncrement](mongodb-bson-timestampinterface.getincrement.md) - Повертає інкрементний компонент TimestampInterface
-   [MongoDBBSONTimestampInterface::getTimestamp](mongodb-bson-timestampinterface.gettimestamp.md) — Повертає компонент позначки часу TimestampInterface
-   [MongoDBBSONTimestampInterface::toString](mongodb-bson-timestampinterface.tostring.md) — Повертає строкову виставу TimestampInterface
