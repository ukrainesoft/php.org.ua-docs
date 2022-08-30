Клас MongoDBBSONSymbol (застарілий)

-   [« MongoDBBSONInt64::unserialize](mongodb-bson-int64.unserialize.html)
    
-   [MongoDBBSONSymbol::construct »](mongodb-bson-symbol.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSON](book.bson.html)
    
-   Клас MongoDBBSONSymbol (застарілий)
    

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
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+. |

## Зміст

-   [MongoDBBSONSymbol::construct](mongodb-bson-symbol.construct.html) — Створює новий Symbol (не використовується)
-   [MongoDBBSONSymbol::jsonSerialize](mongodb-bson-symbol.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONSymbol::serialize](mongodb-bson-symbol.serialize.html) - Серіалізує Symbol
-   [MongoDBBSONSymbol::toString](mongodb-bson-symbol.tostring.html) — Повертає Symbol у вигляді рядка
-   [MongoDBBSONSymbol::unserialize](mongodb-bson-symbol.unserialize.html) - Десеріалізує Symbol