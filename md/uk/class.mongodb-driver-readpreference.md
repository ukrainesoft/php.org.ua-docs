Клас MongoDBDriverReadPreference

-   [« MongoDBDriverWriteConcern::unserialize](mongodb-driver-writeconcern.unserialize.html)
    
-   [MongoDBDriverReadPreference::bsonSerialize »](mongodb-driver-readpreference.bsonserialize.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriver](book.mongodb.md)
    
-   Клас MongoDBDriverReadPreference
    

# Клас MongoDBDriverReadPreference

(mongodb >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\ReadPreference
     

     implements 
       MongoDB\BSON\Serializable,  Serializable {
    
    /* Константы */
    
     const
     int
      RP_PRIMARY = 1;

    const
     int
      RP_PRIMARY_PREFERRED = 5;

    const
     int
      RP_SECONDARY = 2;

    const
     int
      RP_SECONDARY_PREFERRED = 6;

    const
     int
      RP_NEAREST = 10;

    const
     string
      PRIMARY = primary;

    const
     string
      PRIMARY_PREFERRED = primaryPreferred;

    const
     string
      SECONDARY = secondary;

    const
     string
      SECONDARY_PREFERRED = secondaryPreferred;

    const
     string
      NEAREST = nearest;

    const
     int
      NO_MAX_STALENESS = -1;

    const
     int
      SMALLEST_MAX_STALENESS_SECONDS = 90;


    /* Методы */
    
   final public bsonSerialize(): object
final public __construct(string|int $mode, ?array $tagSets = null, ?array $options = null)
final public getHedge(): ?object
final public getMaxStalenessSeconds(): int
final public getMode(): int
final public getModeString(): string
final public getTagSets(): array
final public serialize(): string
final public unserialize(string $serialized): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\ReadPreference::RP_PRIMARY`**

Усі операції зчитуються з поточного первинного вузла реплік набору. Це перевага для читання за промовчанням для MongoDB.

**`MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED`**

У більшості ситуація операції зчитуються з первинного вузла, але якщо він недоступний, операції зчитуються з вторинних членів.

**`MongoDB\Driver\ReadPreference::RP_SECONDARY`**

Усі операції зчитуються із вторинних членів набору реплік.

**`MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED`**

Здебільшого ситуація операції зчитуються з вторинних вузлів, але якщо вони недоступні, операції зчитуються з первинного вузла.

**`MongoDB\Driver\ReadPreference::RP_NEAREST`**

Операції зчитуються з члена набору реплік із найменшою затримкою мережі, незалежно від типу члена.

**`MongoDB\Driver\ReadPreference::PRIMARY`**

Усі операції з поточної репліки встановлені первинними. Це перевага для читання за промовчанням для MongoDB.

**`MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED`**

Найчастіше операції читаються з первинного вузла, але якщо він недоступний, операції читаються з вторинних вузлів.

**`MongoDB\Driver\ReadPreference::SECONDARY`**

Усі операції читаються із вторинних вузлів набору реплік.

**`MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED`**

Найчастіше операції читаються з вторинних вузлів, але якщо вони недоступні, операції читаються з первинного.

**`MongoDB\Driver\ReadPreference::NEAREST`**

Операції зчитуються з вузла набору реплік із найменшою затримкою в мережі незалежно від типу.

**`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`**

Значення за промовчанням для параметра `"maxStalenessSeconds"` щоб вказати на обмеження на максимальне запізнення (Staleness), що означає, що драйвер не враховуватиме затримку вторинних вузлів при виборі напрямку для операції читання.

**`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS`**

Мінімальне значення для параметра `"maxStalenessSeconds"` дорівнює 90 секунд. Драйвер оцінює запізнення вторинних вузлів, періодично перевіряючи останню дату запису кожного члена набору реплік. Оскільки ці перевірки нечасті, оцінка запізнення є грубою. Таким чином, драйвер не може забезпечити максимальну величину запізнення менше 90 секунд.

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.7.0 |  |
| Додані константи **`MongoDB\Driver\ReadPreference::PRIMARY`** **`MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED`** **`MongoDB\Driver\ReadPreference::SECONDARY`** **`MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED`** **`MongoDB\Driver\ReadPreference::NEAREST`** |  |

Реалізує [Serializable](class.serializable.md)

| | PECL mongodb 1.2.0

Додані константи **`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`** і **`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS`**

Реалізує [MongoDBBSONSerializable](class.mongodb-bson-serializable.html)

## Зміст

-   [MongoDBDriverReadPreference::bsonSerialize](mongodb-driver-readpreference.bsonserialize.html) — Повертає об'єкт серіалізації BSON
-   [MongoDBDriverReadPreference::construct](mongodb-driver-readpreference.construct.html) — Створити новий ReadPreference
-   [MongoDBDriverReadPreference::getHedge](mongodb-driver-readpreference.gethedge.html) — Повертає опцію "hedge" із ReadPreference
-   [MongoDBDriverReadPreference::getMaxStalenessSeconds](mongodb-driver-readpreference.getmaxstalenessseconds.html) — Повертає параметр "maxStalenessSeconds" ReadPreference
-   [MongoDBDriverReadPreference::getMode](mongodb-driver-readpreference.getmode.html) - Повертає параметр "mode" ReadPreference
-   [MongoDBDriverReadPreference::getModeString](mongodb-driver-readpreference.getmodestring.html) - Повертає опцію "mode" об'єкта ReadPreference у вигляді рядка
-   [MongoDBDriverReadPreference::getTagSets](mongodb-driver-readpreference.gettagsets.html) - Повертає параметр "tagSets" ReadPreference
-   [MongoDBDriverReadPreference::serialize](mongodb-driver-readpreference.serialize.html) — Серіалізація ReadPreference
-   [MongoDBDriverReadPreference::unserialize](mongodb-driver-readpreference.unserialize.html) - Десеріалізація ReadPreference