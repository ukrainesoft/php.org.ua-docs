---
navigation:
  - class.mongodb-bson-persistable.md: « MongoDB\\BSON\\Persistable
  - class.mongodb-bson-serializable.md: MongoDB\\BSON\\Serializable »
  - index.md: PHP Manual
  - class.mongodb-bson-persistable.md: MongoDB\\BSON\\Persistable
title: 'MongoDB\\BSON\\Persistable::bsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Persistable::bsonSerialize

(mongodb >=1.0.0)

MongoDB\\BSON\\Persistable::bsonSerialize — Надає масив або документ для серіалізації у форматі BSON

### Опис

```methodsynopsis
abstract public MongoDB\BSON\Persistable::bsonSerialize(): array|stdClass|MongoDB\BSON\Document
```

Викликається під час серіалізації об'єкта в BSON. Метод повинен повертати масив (array), [stdClass](class.stdclass.md) або [MongoDB\\BSON\\Document](class.mongodb-bson-document.md)

Значення, що повертається, завжди буде серіалізоване у вигляді BSON-документа. Серіалізований документ включатиме поле, що містить ім'я класу об'єкта. Тому в даному методі неможливо повернути екземпляр класу [MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md)

Користувачам рекомендується включати властивість \_id (например,[MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md), ініціалізоване у вашому конструкторі) при поверненні даних для кореневого документа BSON; інакше драйверу або базі даних доведеться генерувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) при додаванні чи оновленні документа, відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Массив (array),[stdClass](class.stdclass.md) або [MongoDB\\BSON\\Document](class.mongodb-bson-document.md), який має бути серіалізований у вигляді BSON-документу.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.17.0 |  |
| Тепер метод може також повертати екземпляри [MongoDB\\BSON\\Document](class.mongodb-bson-document.md) на додаток до масиву (array) та [stdClass](class.stdclass.md) |  |

### Дивіться також

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) \- Надає масив або документ для серіалізації у BSON
-   [MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md) \- Створює об'єкт із масиву BSON або документа
-   [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md)
-   [Постійні дані](mongodb.persistence.md)
