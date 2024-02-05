---
navigation:
  - mongodb-driver-serverapi.unserialize.md: '« MongoDB\\Driver\\ServerApi::unserialize'
  - mongodb-driver-writeconcern.bsonserialize.md: 'MongoDB\\Driver\\WriteConcern::bsonSerialize »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\WriteConcern
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\WriteConcern

(mongodb >=1.0.0)

## Вступ

**MongoDB\\Driver\\WriteConcern** описує рівень надійності, запрошений MongoDB для операцій запису на автономний `mongod` або на набір реплік або сегментовані кластери. У сегментованих кластерах екземпляри `mongos` будуть передавати гарантії запису на сегменти.

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
    
   final public bsonSerialize(): stdClass
final public __construct(string|int $w, ?int $wtimeout = null, ?bool $journal = null)
final public getJournal(): ?bool
final public getW(): string|int|null
final public getWtimeout(): int
final public isDefault(): bool
final public serialize(): string
final public unserialize(string $data): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\WriteConcern::MAJORITY`**

Більшість членів у наборі; арбітрів, члени, які не беруть участь у голосуванні, пасивні члени, приховані члени та відкладені члени, всі вони включені до визначення більшості гарантії запису.

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.7.0 | Реалізує [Serializable](class.serializable.md) |
| PECL mongodb 1.2.0 | Реалізує [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md) |

## Зміст

-   [MongoDB\\Driver\\WriteConcern::bsonSerialize](mongodb-driver-writeconcern.bsonserialize.md)— Повертає об'єкт серіалізації BSON
-   [MongoDB\\Driver\\WriteConcern::\_\_construct](mongodb-driver-writeconcern.construct.md) \- Створити новий WriteConcern
-   [MongoDB\\Driver\\WriteConcern::getJournal](mongodb-driver-writeconcern.getjournal.md) — Повертає опцію journal WriteConcern
-   [MongoDB\\Driver\\WriteConcern::getW](mongodb-driver-writeconcern.getw.md) - Повертає опцію "w" WriteConcern
-   [MongoDB\\Driver\\WriteConcern::getWtimeout](mongodb-driver-writeconcern.getwtimeout.md) - Повертає опцію "wtimeout" WriteConcern
-   [MongoDB\\Driver\\WriteConcern::isDefault](mongodb-driver-writeconcern.isdefault.md)— Перевіряє, чи є гарантія запису за замовчуванням
-   [MongoDB\\Driver\\WriteConcern::serialize](mongodb-driver-writeconcern.serialize.md) \- Серіалізація WriteConcern
-   [MongoDB\\Driver\\WriteConcern::unserialize](mongodb-driver-writeconcern.unserialize.md) \- Десеріалізація WriteConcern
