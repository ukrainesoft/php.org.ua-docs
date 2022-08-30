Клас MongoDBBSONDBPointer (застарілий)

-   [« MongoDBBSONUTCDateTimeInterface::toString](mongodb-bson-utcdatetimeinterface.tostring.html)
    
-   [MongoDBBSONDBPointer::construct »](mongodb-bson-dbpointer.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSON](book.bson.html)
    
-   Клас MongoDBBSONDBPointer (застарілий)
    

# Клас MongoDBBSONDBPointer (застарілий)

(mongodb >=1.4.0)

## Вступ

Тип BSON типу "DBPointer". Цей тип BSON застарів і цей клас не може бути створений. Він буде створений з типу BSON DBPointer під час перетворення BSON на PHP, а також при перетворенні назад на BSON при зберіганні документів у базі даних.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\BSON\DBPointer
     

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

| Версия              | Описание                                                             |
|---------------------|----------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+. |

## Зміст

-   [MongoDBBSONDBPointer::construct](mongodb-bson-dbpointer.construct.html) — Створює новий DBPointer (не використовується)
-   [MongoDBBSONDBPointer::jsonSerialize](mongodb-bson-dbpointer.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONDBPointer::serialize](mongodb-bson-dbpointer.serialize.html) - Серіалізує DBPointer
-   [MongoDBBSONDBPointer::toString](mongodb-bson-dbpointer.tostring.html) — Повертає порожній рядок
-   [MongoDBBSONDBPointer::unserialize](mongodb-bson-dbpointer.unserialize.html) - Десеріалізує DBPointer