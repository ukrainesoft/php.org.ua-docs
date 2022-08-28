Клас MongoDBBSONDBPointer (застарілий)

-   [« MongoDB\\BSON\\UTCDateTimeInterface::\_\_toString](mongodb-bson-utcdatetimeinterface.tostring.html)
    
-   [MongoDB\\BSON\\DBPointer::\_\_construct »](mongodb-bson-dbpointer.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
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

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+. |

## Зміст

-   [MongoDB\\BSON\\DBPointer::\_\_construct](mongodb-bson-dbpointer.construct.html) — Створює новий DBPointer (не використовується)
-   [MongoDB\\BSON\\DBPointer::jsonSerialize](mongodb-bson-dbpointer.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\DBPointer::serialize](mongodb-bson-dbpointer.serialize.html) - Серіалізує DBPointer
-   [MongoDB\\BSON\\DBPointer::\_\_toString](mongodb-bson-dbpointer.tostring.html) — Повертає порожній рядок
-   [MongoDB\\BSON\\DBPointer::unserialize](mongodb-bson-dbpointer.unserialize.html) - Десеріалізує DBPointer