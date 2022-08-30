Клас MongoDBBSONObjectId

-   [« MongoDBBSONMinKey::unserialize](mongodb-bson-minkey.unserialize.html)
    
-   [MongoDBBSONObjectId::construct »](mongodb-bson-objectid.construct.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSON](book.bson.md)
    
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

-   Час створення ObjectId можна отримати за допомогою методу [MongoDBBSONObjectId::getTimestamp()](mongodb-bson-objectid.gettimestamp.html)
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
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 |  |
| Перейменований з `MongoDB\BSON\ObjectID` в `MongoDB\BSON\ObjectId` |  |

Реалізує інтерфейс [MongoDBBSONObjectIdInterface](class.mongodb-bson-objectidinterface.html)

| | PECL mongodb 1.2.0 Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md).

## Зміст

-   [MongoDBBSONObjectId::construct](mongodb-bson-objectid.construct.html) - Створює новий ObjectId
-   [MongoDBBSONObjectId::getTimestamp](mongodb-bson-objectid.gettimestamp.html) — Повертає позначку часу ObjectId
-   [MongoDBBSONObjectId::jsonSerialize](mongodb-bson-objectid.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONObjectId::serialize](mongodb-bson-objectid.serialize.html) - Серіалізує ObjectId
-   [MongoDBBSONObjectId::toString](mongodb-bson-objectid.tostring.html) — Повертає шістнадцяткову виставу ObjectId
-   [MongoDBBSONObjectId::unserialize](mongodb-bson-objectid.unserialize.html) - Десеріалізує ObjectId