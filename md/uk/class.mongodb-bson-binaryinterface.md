Інтерфейс MongoDBBSONBinaryInterface

-   [« MongoDBBSONUnserializable::bsonUnserialize](mongodb-bson-unserializable.bsonunserialize.html)
    
-   [MongoDBBSONBinaryInterface::getData »](mongodb-bson-binaryinterface.getdata.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSON](book.bson.md)
    
-   Інтерфейс MongoDBBSONBinaryInterface
    

# Інтерфейс MongoDBBSONBinaryInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDBBSONBinary](class.mongodb-bson-binary.html), але також може використовуватися як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONBinaryInterface::getData](mongodb-bson-binaryinterface.getdata.html) — Повертає дані BinaryInterface
-   [MongoDBBSONBinaryInterface::getType](mongodb-bson-binaryinterface.gettype.html) — Повертає тип BinaryInterface
-   [MongoDBBSONBinaryInterface::toString](mongodb-bson-binaryinterface.tostring.html) — Повертає дані BinaryInterface