Клас MongoDBDriverWriteConcern

-   [« MongoDB\\Driver\\ServerApi::unserialize](mongodb-driver-serverapi.unserialize.html)
    
-   [MongoDB\\Driver\\WriteConcern::bsonSerialize »](mongodb-driver-writeconcern.bsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver](book.mongodb.html)
    
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

| Версия             | Описание                                                                     |
|--------------------|------------------------------------------------------------------------------|
| PECL mongodb 1.7.0 | Реалізує [Serializable](class.serializable.html)                             |
| PECL mongodb 1.2.0 | Реалізує [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html) |

## Зміст

-   [MongoDB\\Driver\\WriteConcern::bsonSerialize](mongodb-driver-writeconcern.bsonserialize.html) — Повертає об'єкт серіалізації BSON
-   [MongoDB\\Driver\\WriteConcern::\_\_construct](mongodb-driver-writeconcern.construct.html) - Створити новий WriteConcern
-   [MongoDB\\Driver\\WriteConcern::getJournal](mongodb-driver-writeconcern.getjournal.html) — Повертає опцію journal WriteConcern
-   [MongoDB\\Driver\\WriteConcern::getW](mongodb-driver-writeconcern.getw.html) - Повертає опцію "w" WriteConcern
-   [MongoDB\\Driver\\WriteConcern::getWtimeout](mongodb-driver-writeconcern.getwtimeout.html) - Повертає опцію "wtimeout" WriteConcern
-   [MongoDB\\Driver\\WriteConcern::isDefault](mongodb-driver-writeconcern.isdefault.html) — Перевіряє, чи є гарантія запису за замовчуванням
-   [MongoDB\\Driver\\WriteConcern::serialize](mongodb-driver-writeconcern.serialize.html) - Серіалізація WriteConcern
-   [MongoDB\\Driver\\WriteConcern::unserialize](mongodb-driver-writeconcern.unserialize.html) - Десеріалізація WriteConcern