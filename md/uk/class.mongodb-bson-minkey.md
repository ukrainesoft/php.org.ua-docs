Клас MongoDBBSONMinKey

-   [« MongoDBBSONMaxKey::unserialize](mongodb-bson-maxkey.unserialize.html)
    
-   [MongoDBBSONMinKey::construct »](mongodb-bson-minkey.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSON](book.bson.html)
    
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
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDBBSONMinKeyInterface](class.mongodb-bson-minkeyinterface.html)                      |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDBBSONMinKey::construct](mongodb-bson-minkey.construct.html) - Конструктор MinKey
-   [MongoDBBSONMinKey::jsonSerialize](mongodb-bson-minkey.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONMinKey::serialize](mongodb-bson-minkey.serialize.html) - Серіалізує MinKey
-   [MongoDBBSONMinKey::unserialize](mongodb-bson-minkey.unserialize.html) - Десеріалізує MinKey