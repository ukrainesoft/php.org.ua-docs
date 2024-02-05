---
navigation:
  - mongodb-bson-persistable.bsonserialize.md: '« MongoDB\\BSON\\Persistable::bsonSerialize'
  - mongodb-bson-serializable.bsonserialize.md: 'MongoDB\\BSON\\Serializable::bsonSerialize »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\Serializable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\Serializable

(mongodb >=1.0.0)

## Вступ

Класи, які реалізують цей інтерфейс можуть повертати дані для серіалізації у вигляді масиву BSON або документа замість відкритих властивостей об'єкта.

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\BSON\Serializable
     

     implements 
       MongoDB\BSON\Type {


    /* Методы */
    
   abstract public bsonSerialize(): array|stdClass|MongoDB\BSON\Document|MongoDB\BSON\PackedArray

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\Serializable::bsonSerialize](mongodb-bson-serializable.bsonserialize.md)— Надає масив або документ для серіалізації у BSON
