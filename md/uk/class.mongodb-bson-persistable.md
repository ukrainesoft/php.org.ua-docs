---
navigation:
  - class.mongodb-bson-type.html: « MongoDBBSONType
  - class.mongodb-bson-serializable.html: MongoDBBSONSerializable »
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Інтерфейс MongoDBBSONPersistable
---
# Інтерфейс MongoDBBSONPersistable

(mongodb >=1.0.0)

## Вступ

Класи можуть реалізовувати цей інтерфейс використання переваг автоматичного ODM (порівняння документів об'єкта) поведінки в драйвері. Під час серіалізації драйвер вставляє властивість pclass, що містить ім'я класу PHP, дані, що повертаються [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html). Під час десеріалізації та ж властивість pclass буде використовуватися для виведення класу PHP (незалежного від будь-якої конфігурації [типу картки](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps)), яка має бути створена до виклику [MongoDBBSONUnserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md). Дивіться [Постійні дані](mongodb.persistence.md) для отримання додаткової інформації.

> **Зауваження**: Навіть якщо [MongoDBBSONSerializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) поверне послідовний масив, використання якості pclass призведе до серіалізації об'єкта як документа BSON.

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\BSON\Persistable
     

     implements 
       MongoDB\BSON\Unserializable,  MongoDB\BSON\Serializable {


    /* Наследуемые методы */
    
   abstract public MongoDB\BSON\Serializable::bsonSerialize(): array|object

    abstract public MongoDB\BSON\Unserializable::bsonUnserialize(array $data): void

   }
```
