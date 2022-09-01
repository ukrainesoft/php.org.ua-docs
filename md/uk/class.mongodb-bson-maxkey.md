---
navigation:
  - mongodb-bson-javascript.unserialize.html: '« MongoDBBSONJavascript::unserialize'
  - mongodb-bson-maxkey.construct.html: 'MongoDBBSONMaxKey::construct »'
  - index.html: PHP Manual
  - book.bson.html: MongoDBBSON
title: Клас MongoDBBSONMaxKey
---
# Клас MongoDBBSONMaxKey

(mongodb >=1.0.0)

## Вступ

Спеціальний тип BSON, який порівнює вище за всіх інших можливих значень елемента BSON.

> **Зауваження**: Це внутрішній тип MongoDB, що використовується для індексації та шардингу.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\MaxKey
     

     implements 
       MongoDB\BSON\MaxKeyInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable {


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
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDBBSONMaxKeyInterface](class.mongodb-bson-maxkeyinterface.html) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDBBSONMaxKey::construct](mongodb-bson-maxkey.construct.html) - Конструктор MaxKey
-   [MongoDBBSONMaxKey::jsonSerialize](mongodb-bson-maxkey.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONMaxKey::serialize](mongodb-bson-maxkey.serialize.html) - Серіалізує MaxKey
-   [MongoDBBSONMaxKey::unserialize](mongodb-bson-maxkey.unserialize.html) - Десеріалізує MaxKey
