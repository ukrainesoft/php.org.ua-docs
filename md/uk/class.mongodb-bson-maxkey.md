---
navigation:
  - mongodb-bson-javascript.unserialize.md: '« MongoDB\\BSON\\Javascript::unserialize'
  - mongodb-bson-maxkey.construct.md: 'MongoDB\\BSON\\MaxKey::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\MaxKey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\MaxKey

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
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\MaxKeyInterface](class.mongodb-bson-maxkeyinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\MaxKey::\_\_construct](mongodb-bson-maxkey.construct.md) \- Конструктор MaxKey
-   [MongoDB\\BSON\\MaxKey::jsonSerialize](mongodb-bson-maxkey.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\MaxKey::serialize](mongodb-bson-maxkey.serialize.md) \- Серіалізує MaxKey
-   [MongoDB\\BSON\\MaxKey::unserialize](mongodb-bson-maxkey.unserialize.md) \- Десеріалізує MaxKey
