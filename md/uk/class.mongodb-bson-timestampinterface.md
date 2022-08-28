Інтерфейс MongoDBBSONTimestampInterface

-   [« MongoDB\\BSON\\RegexInterface::\_\_toString](mongodb-bson-regexinterface.tostring.html)
    
-   [MongoDB\\BSON\\TimestampInterface::getIncrement »](mongodb-bson-timestampinterface.getincrement.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Інтерфейс MongoDBBSONTimestampInterface
    

# Інтерфейс MongoDBBSONTimestampInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.html), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

-   [MongoDB\\BSON\\TimestampInterface::getIncrement](mongodb-bson-timestampinterface.getincrement.html) - Повертає інкрементний компонент TimestampInterface
-   [MongoDB\\BSON\\TimestampInterface::getTimestamp](mongodb-bson-timestampinterface.gettimestamp.html) — Повертає компонент позначки часу TimestampInterface
-   [MongoDB\\BSON\\TimestampInterface::\_\_toString](mongodb-bson-timestampinterface.tostring.html) — Повертає строкову виставу TimestampInterface