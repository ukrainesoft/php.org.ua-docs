---
navigation:
  - mongodb-bson-symbol.unserialize.html: '« MongoDBBSONSymbol::unserialize'
  - mongodb-bson-undefined.construct.html: 'MongoDBBSONUndefined::construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Клас MongoDBBSONUndefined (застаріло)
---
# Клас MongoDBBSONUndefined (застаріло)

(mongodb >=1.4.0)

## Вступ

Тип BSON типу "Undefined". Цей тип BSON застарів і цей клас не може бути створений. Він буде створений з невизначеного типу BSON під час перетворення BSON на PHP, а також може бути перетворений назад на BSON при зберіганні документів у базі даних.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\Undefined
     

     implements 
       MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {


    /* Методы */
    
   final private __construct()
final public jsonSerialize(): mixed
final public serialize(): string
final public __toString(): string
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |

## Зміст

-   [MongoDBBSONUndefined::construct](mongodb-bson-undefined.construct.html) - Створює новий Undefined (не використовується)
-   [MongoDBBSONUndefined::jsonSerialize](mongodb-bson-undefined.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONUndefined::serialize](mongodb-bson-undefined.serialize.html) - Серіалізує Undefined
-   [MongoDBBSONUndefined::toString](mongodb-bson-undefined.tostring.html) — Повертає порожній рядок
-   [MongoDBBSONUndefined::unserialize](mongodb-bson-undefined.unserialize.html) - Десеріалізує Undefined
