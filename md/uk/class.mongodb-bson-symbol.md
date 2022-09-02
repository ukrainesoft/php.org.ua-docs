---
navigation:
  - mongodb-bson-int64.unserialize.md: '« MongoDBBSONInt64::unserialize'
  - mongodb-bson-symbol.construct.md: 'MongoDBBSONSymbol::construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Клас MongoDBBSONSymbol (застарілий)
---
# Клас MongoDBBSONSymbol (застарілий)

(mongodb >=1.4.0)

## Вступ

Тип BSON типу "Symbol". Цей тип BSON застарів і цей клас не може бути створений. Він буде створений з типу символу BSON під час перетворення BSON на PHP, а також при перетворенні назад на BSON при зберіганні документів у базі даних.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\BSON\Symbol
     

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

-   [MongoDBBSONSymbol::construct](mongodb-bson-symbol.construct.md) — Створює новий Symbol (не використовується)
-   [MongoDBBSONSymbol::jsonSerialize](mongodb-bson-symbol.jsonserialize.md) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONSymbol::serialize](mongodb-bson-symbol.serialize.md) - Серіалізує Symbol
-   [MongoDBBSONSymbol::toString](mongodb-bson-symbol.tostring.md) — Повертає Symbol у вигляді рядка
-   [MongoDBBSONSymbol::unserialize](mongodb-bson-symbol.unserialize.md) - Десеріалізує Symbol
