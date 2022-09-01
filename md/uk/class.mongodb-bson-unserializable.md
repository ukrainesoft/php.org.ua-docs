---
navigation:
  - mongodb-bson-serializable.bsonserialize.html: '« MongoDBBSONSerializable::bsonSerialize'
  - mongodb-bson-unserializable.bsonunserialize.html: 'MongoDBBSONUnserializable::bsonUnserialize »'
  - index.html: PHP Manual
  - book.bson.html: MongoDBBSON
title: Інтерфейс MongoDBBSONUnserializable
---
# Інтерфейс MongoDBBSONUnserializable

(mongodb >=1.0.0)

## Вступ

Класи, які реалізують цей інтерфейс, можуть бути вказані в [карте типов](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps) для десеріалізації масивів та документів BSON (як кореневих, так і вбудованих).

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\BSON\Unserializable
     
     {


    /* Методы */
    
   abstract public bsonUnserialize(array $data): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONUnserializable::bsonUnserialize](mongodb-bson-unserializable.bsonunserialize.html) — Створює об'єкт із масиву BSON або документа
