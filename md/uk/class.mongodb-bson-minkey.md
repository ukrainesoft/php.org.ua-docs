---
navigation:
  - mongodb-bson-maxkey.unserialize.md: '« MongoDB\\BSON\\MaxKey::unserialize'
  - mongodb-bson-minkey.construct.md: 'MongoDB\\BSON\\MinKey::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\MinKey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\MinKey

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
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\MinKeyInterface](class.mongodb-bson-minkeyinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\MinKey::\_\_construct](mongodb-bson-minkey.construct.md) \- Конструктор MinKey
-   [MongoDB\\BSON\\MinKey::jsonSerialize](mongodb-bson-minkey.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\MinKey::serialize](mongodb-bson-minkey.serialize.md) \- Серіалізує MinKey
-   [MongoDB\\BSON\\MinKey::unserialize](mongodb-bson-minkey.unserialize.md) \- Десеріалізує MinKey
