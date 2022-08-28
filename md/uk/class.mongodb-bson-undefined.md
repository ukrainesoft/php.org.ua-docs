Клас MongoDBBSONUndefined (застаріло)

-   [« MongoDB\\BSON\\Symbol::unserialize](mongodb-bson-symbol.unserialize.html)
    
-   [MongoDB\\BSON\\Undefined::\_\_construct »](mongodb-bson-undefined.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Клас MongoDBBSONUndefined (застаріло)
    

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

| Версия              | Описание                                                             |
|---------------------|----------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+. |

## Зміст

-   [MongoDB\\BSON\\Undefined::\_\_construct](mongodb-bson-undefined.construct.html) - Створює новий Undefined (не використовується)
-   [MongoDB\\BSON\\Undefined::jsonSerialize](mongodb-bson-undefined.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Undefined::serialize](mongodb-bson-undefined.serialize.html) - Серіалізує Undefined
-   [MongoDB\\BSON\\Undefined::\_\_toString](mongodb-bson-undefined.tostring.html) — Повертає порожній рядок
-   [MongoDB\\BSON\\Undefined::unserialize](mongodb-bson-undefined.unserialize.html) - Десеріалізує Undefined