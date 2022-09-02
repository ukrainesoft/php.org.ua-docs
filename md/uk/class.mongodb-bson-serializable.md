---
navigation:
  - class.mongodb-bson-persistable.md: « MongoDBBSONPersistable
  - mongodb-bson-serializable.bsonserialize.md: 'MongoDBBSONSerializable::bsonSerialize »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Інтерфейс MongoDBBSONSerializable
---
# Інтерфейс MongoDBBSONSerializable

(mongodb >=1.0.0)

## Вступ

Класи, які реалізують цей інтерфейс можуть повертати дані для серіалізації у вигляді масиву BSON або документа замість відкритих властивостей об'єкта.

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\BSON\Serializable
     

     implements 
       MongoDB\BSON\Type {


    /* Методы */
    
   abstract public bsonSerialize(): array|object

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONSerializable::bsonSerialize](mongodb-bson-serializable.bsonserialize.md) — Надає масив або документ для серіалізації у BSON
