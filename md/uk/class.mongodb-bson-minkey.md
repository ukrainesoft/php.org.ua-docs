---
navigation:
  - mongodb-bson-maxkey.unserialize.html: '« MongoDBBSONMaxKey::unserialize'
  - mongodb-bson-minkey.construct.html: 'MongoDBBSONMinKey::construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Клас MongoDBBSONMinKey
---
# Клас MongoDBBSONMinKey

(mongodb >=1.0.0)

## Вступ

Спеціальний тип BSON, який порівнює нижче від усіх інших можливих значень елемента BSON.

> **Зауваження**: Це внутрішній тип MongoDB, що використовується для індексації та шардингу.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\MinKey
     

     implements 
       MongoDB\BSON\MinKeyInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable {
    

    /* Методы */
    
   final public __construct()
final public jsonSerialize(): mixed
final public serialize(): string
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDBBSONMinKeyInterface](class.mongodb-bson-minkeyinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDBBSONMinKey::construct](mongodb-bson-minkey.construct.md) - Конструктор MinKey
-   [MongoDBBSONMinKey::jsonSerialize](mongodb-bson-minkey.jsonserialize.md) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONMinKey::serialize](mongodb-bson-minkey.serialize.md) - Серіалізує MinKey
-   [MongoDBBSONMinKey::unserialize](mongodb-bson-minkey.unserialize.md) - Десеріалізує MinKey
