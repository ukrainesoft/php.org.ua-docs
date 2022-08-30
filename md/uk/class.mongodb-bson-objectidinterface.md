Інтерфейс MongoDBBSONObjectIdInterface

-   [« MongoDBBSONMinKeyInterface](class.mongodb-bson-minkeyinterface.html)
    
-   [MongoDBBSONObjectIdInterface::getTimestamp »](mongodb-bson-objectidinterface.gettimestamp.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSON](book.bson.md)
    
-   Інтерфейс MongoDBBSONObjectIdInterface
    

# Інтерфейс MongoDBBSONObjectIdInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізований за допомогою [MongoDBBSONObjectId](class.mongodb-bson-objectid.html), але також може бути використаний як параметр, що повертається значення або типу властивості в класах користувальницького простору.

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

| Версия              | Описание                                                                                                                                                                                                                                                                                                                |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONObjectIdInterface::getTimestamp](mongodb-bson-objectidinterface.gettimestamp.html) — Повертає компонент позначки часу ObjectIdInterface
-   [MongoDBBSONObjectIdInterface::toString](mongodb-bson-objectidinterface.tostring.html) — Повертає шістнадцяткову виставу ObjectIdInterface