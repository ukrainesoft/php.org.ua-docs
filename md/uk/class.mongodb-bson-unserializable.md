---
navigation:
  - mongodb-bson-serializable.bsonserialize.md: '« MongoDB\\BSON\\Serializable::bsonSerialize'
  - mongodb-bson-unserializable.bsonunserialize.md: 'MongoDB\\BSON\\Unserializable::bsonUnserialize »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\Unserializable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\Unserializable

(mongodb >=1.0.0)

## Вступ

Класи, які реалізують цей інтерфейс, можуть бути вказані в [карті типів](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps) для десеріалізації масивів та документів BSON (як кореневих, так і вбудованих).

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\BSON\Unserializable
     
     {


    /* Методы */
    
   abstract public bsonUnserialize(array $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\Unserializable::bsonUnserialize](mongodb-bson-unserializable.bsonunserialize.md)— Створює об'єкт із масиву BSON або документа
