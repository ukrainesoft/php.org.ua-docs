---
navigation:
  - class.mongodb-bson-type.md: « MongoDB\\BSON\\Type
  - mongodb-bson-persistable.bsonserialize.md: 'MongoDB\\BSON\\Persistable::bsonSerialize »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\Persistable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\Persistable

(mongodb >=1.0.0)

## Вступ

Класи можуть реалізовувати цей інтерфейс використання переваг автоматичного ODM (порівняння документів об'єкта) поведінки в драйвері. Під час серіалізації драйвер вставляє властивість \_\_pclass, що містить ім'я класу PHP, дані, що повертаються [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md)Во время десериализации то же свойство\_\_pclass буде використовуватися для виведення класу PHP (незалежного від будь-якої конфігурації [типу картки](mongodb.persistence.deserialization.md#mongodb.persistence.typemaps)), яка має бути створена до виклику [MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md)Смотрите[Постійні дані](mongodb.persistence.md) для отримання додаткової інформації.

> **Зауваження**: Навіть якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) поверне послідовний масив, використання якості \_\_pclass призведе до серіалізації об'єкта як документа BSON.

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\BSON\Persistable
     

     implements 
       MongoDB\BSON\Unserializable,  MongoDB\BSON\Serializable {


    /* Методы */
    
   abstract public bsonSerialize(): array|stdClass|MongoDB\BSON\Document


    /* Наследуемые методы */
    abstract public MongoDB\BSON\Serializable::bsonSerialize(): array|stdClass|MongoDB\BSON\Document|MongoDB\BSON\PackedArray

    abstract public MongoDB\BSON\Unserializable::bsonUnserialize(array $data): void

   }
```

## Зміст

-   [MongoDB\\BSON\\Persistable::bsonSerialize](mongodb-bson-persistable.bsonserialize.md)— Надає масив або документ для серіалізації у форматі BSON
