Клас MongoDBDriverWriteConcern

-   [« MongoDBDriverServerApi::unserialize](mongodb-driver-serverapi.unserialize.html)
    
-   [MongoDBDriverWriteConcern::bsonSerialize »](mongodb-driver-writeconcern.bsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriver](book.mongodb.html)
    
-   Клас MongoDBDriverWriteConcern
    

# Клас MongoDBDriverWriteConcern

(mongodb >=1.0.0)

## Вступ

**MongoDBDriverWriteConcern** описує рівень надійності, запрошений MongoDB для операцій запису на автономний `mongod` або на набір реплік або сегментовані кластери. У сегментованих кластерах екземпляри `mongos` будуть передавати гарантії запису на сегменти.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\WriteConcern
     

     implements 
       MongoDB\BSON\Serializable,  Serializable {
    
    /* Константы */
    
     const
     string
      MAJORITY = "majority";


    /* Методы */
    
   final public bsonSerialize(): object
final public __construct(string|int $w, ?int $wtimeout = null, ?bool $journal = null)
final public getJournal(): ?bool
final public getW(): string|int|null
final public getWtimeout(): int
final public isDefault(): bool
final public serialize(): string
final public unserialize(string $serialized): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\WriteConcern::MAJORITY`**

Більшість членів у наборі; арбітрів, члени, які не беруть участь у голосуванні, пасивні члени, приховані члени та відкладені члени, всі вони включені до визначення більшості гарантії запису.

## список змін

| Версия             | Описание                                                                 |
|--------------------|--------------------------------------------------------------------------|
| PECL mongodb 1.7.0 | Реалізує [Serializable](class.serializable.html)                         |
| PECL mongodb 1.2.0 | Реалізує [MongoDBBSONSerializable](class.mongodb-bson-serializable.html) |

## Зміст

-   [MongoDBDriverWriteConcern::bsonSerialize](mongodb-driver-writeconcern.bsonserialize.html) — Повертає об'єкт серіалізації BSON
-   [MongoDBDriverWriteConcern::construct](mongodb-driver-writeconcern.construct.html) - Створити новий WriteConcern
-   [MongoDBDriverWriteConcern::getJournal](mongodb-driver-writeconcern.getjournal.html) — Повертає опцію journal WriteConcern
-   [MongoDBDriverWriteConcern::getW](mongodb-driver-writeconcern.getw.html) - Повертає опцію "w" WriteConcern
-   [MongoDBDriverWriteConcern::getWtimeout](mongodb-driver-writeconcern.getwtimeout.html) - Повертає опцію "wtimeout" WriteConcern
-   [MongoDBDriverWriteConcern::isDefault](mongodb-driver-writeconcern.isdefault.html) — Перевіряє, чи є гарантія запису за замовчуванням
-   [MongoDBDriverWriteConcern::serialize](mongodb-driver-writeconcern.serialize.html) - Серіалізація WriteConcern
-   [MongoDBDriverWriteConcern::unserialize](mongodb-driver-writeconcern.unserialize.html) - Десеріалізація WriteConcern