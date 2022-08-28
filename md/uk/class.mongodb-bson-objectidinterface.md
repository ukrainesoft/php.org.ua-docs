Інтерфейс MongoDBBSONObjectIdInterface

-   [« MongoDB\\BSON\\MinKeyInterface](class.mongodb-bson-minkeyinterface.html)
    
-   [MongoDB\\BSON\\ObjectIdInterface::getTimestamp »](mongodb-bson-objectidinterface.gettimestamp.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Інтерфейс MongoDBBSONObjectIdInterface
    

# Інтерфейс MongoDBBSONObjectIdInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html), але також може бути використаний як параметр, що повертається значення або типу властивості в класах користувальницького простору.

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

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\ObjectIdInterface::getTimestamp](mongodb-bson-objectidinterface.gettimestamp.html) — Повертає компонент позначки часу ObjectIdInterface
-   [MongoDB\\BSON\\ObjectIdInterface::\_\_toString](mongodb-bson-objectidinterface.tostring.html) — Повертає шістнадцяткову виставу ObjectIdInterface