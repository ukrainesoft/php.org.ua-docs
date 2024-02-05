---
navigation:
  - mongodb-bson-regexinterface.tostring.md: '« MongoDB\\BSON\\RegexInterface::\_\_function toString() { [native code] }'
  - mongodb-bson-timestampinterface.getincrement.md: 'MongoDB\\BSON\\TimestampInterface::getIncrement »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\TimestampInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\TimestampInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.md), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\TimestampInterface::getIncrement](mongodb-bson-timestampinterface.getincrement.md) \- Повертає інкрементний компонент TimestampInterface
-   [MongoDB\\BSON\\TimestampInterface::getTimestamp](mongodb-bson-timestampinterface.gettimestamp.md)— Повертає компонент позначки часу TimestampInterface
-   [MongoDB\\BSON\\TimestampInterface::\_\_function toString() { \[native code\] }](mongodb-bson-timestampinterface.tostring.md)— Повертає строкову виставу TimestampInterface
