Клас MongoDBBSONMinKey

-   [« MongoDB\\BSON\\MaxKey::unserialize](mongodb-bson-maxkey.unserialize.html)
    
-   [MongoDB\\BSON\\MinKey::\_\_construct »](mongodb-bson-minkey.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Клас MongoDBBSONMinKey
    

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

| Версия             | Описание                                                                                                      |
|--------------------|---------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\MinKeyInterface](class.mongodb-bson-minkeyinterface.html)                  |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDB\\BSON\\MinKey::\_\_construct](mongodb-bson-minkey.construct.html) - Конструктор MinKey
-   [MongoDB\\BSON\\MinKey::jsonSerialize](mongodb-bson-minkey.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\MinKey::serialize](mongodb-bson-minkey.serialize.html) - Серіалізує MinKey
-   [MongoDB\\BSON\\MinKey::unserialize](mongodb-bson-minkey.unserialize.html) - Десеріалізує MinKey