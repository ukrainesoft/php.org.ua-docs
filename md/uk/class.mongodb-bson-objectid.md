Клас MongoDBBSONObjectId

-   [« MongoDB\\BSON\\MinKey::unserialize](mongodb-bson-minkey.unserialize.html)
    
-   [MongoDB\\BSON\\ObjectId::\_\_construct »](mongodb-bson-objectid.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Клас MongoDBBSONObjectId
    

# Клас MongoDBBSONObjectId

(mongodb >=1.0.0)

## Вступ

Тип BSON для [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid). Значення складається з 12 байтів, де перші чотири байти є міткою часу, що відбиває створення ObjectId. Зокрема, значення складається з:

-   4-байтове значення, що становить секунди з початку епохи Unix,
-   5-байтове випадкове число, унікальне для машини та процесу, та
-   3-байтовий лічильник, що починається з випадкового значення.

У MongoDB кожен документ, який зберігається в колекції, вимагає унікального поля `_id`що діє як первинний ключ. Якщо у вставленому документі пропущено поле `_id`, драйвер автоматично створює ObjectId для поля `_id`

Використання ObjectIds для поля `_id` забезпечує наступні додаткові переваги:

-   Час створення ObjectId можна отримати за допомогою методу [MongoDB\\BSON\\ObjectId::getTimestamp()](mongodb-bson-objectid.gettimestamp.html)
-   Сортування по полю `_id`, В якому зберігаються значення ObjectId, приблизно еквівалентна сортуванню за часом створення.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\ObjectId
     

     implements 
       MongoDB\BSON\ObjectIdInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {
    

    /* Методы */
    
   final public __construct(?string $id = null)
final public getTimestamp(): int
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
| PECL mongodb 1.3.0 |  |
| Перейменований з `MongoDB\BSON\ObjectID` в `MongoDB\BSON\ObjectId` |  |

Реалізує інтерфейс [MongoDB\\BSON\\ObjectIdInterface](class.mongodb-bson-objectidinterface.html)

| | PECL mongodb 1.2.0 Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html).

## Зміст

-   [MongoDB\\BSON\\ObjectId::\_\_construct](mongodb-bson-objectid.construct.html) - Створює новий ObjectId
-   [MongoDB\\BSON\\ObjectId::getTimestamp](mongodb-bson-objectid.gettimestamp.html) — Повертає позначку часу ObjectId
-   [MongoDB\\BSON\\ObjectId::jsonSerialize](mongodb-bson-objectid.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\ObjectId::serialize](mongodb-bson-objectid.serialize.html) - Серіалізує ObjectId
-   [MongoDB\\BSON\\ObjectId::\_\_toString](mongodb-bson-objectid.tostring.html) — Повертає шістнадцяткову виставу ObjectId
-   [MongoDB\\BSON\\ObjectId::unserialize](mongodb-bson-objectid.unserialize.html) - Десеріалізує ObjectId