---
navigation:
  - mongodb-bson-minkey.unserialize.md: '« MongoDB\\BSON\\MinKey::unserialize'
  - mongodb-bson-objectid.construct.md: 'MongoDB\\BSON\\ObjectId::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\ObjectId
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\ObjectId

(mongodb >=1.0.0)

## Вступ

Тип BSON для[» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid). Значення складається з 12 байтів, де перші чотири байти є міткою часу, що відбиває створення ObjectId. Зокрема, значення складається з:

-   4-байтове значення, що становить секунди з початку епохи Unix,
-   5-байтове випадкове число, унікальне для машини та процесу, та
-   3-байтовий лічильник, що починається з випадкового значення.

У MongoDB кожен документ, що зберігається в колекції, вимагає унікального поля `_id`що діє як первинний ключ. Якщо у вставленому документі пропущено поле `_id`, драйвер автоматично створює ObjectId для поля `_id`

Использование ObjectIds для поля`_id` забезпечує такі додаткові переваги:

-   Час створення ObjectId можна отримати за допомогою методу[MongoDB\\BSON\\ObjectId::getTimestamp()](mongodb-bson-objectid.gettimestamp.md)
-   Сортування по полю`_id`, в якому зберігаються значення ObjectId, приблизно еквівалентна сортуванню за часом створення.

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
final public unserialize(string $data): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 |  |
| Перейменований з `MongoDB\BSON\ObjectID`в`MongoDB\BSON\ObjectId` |  |

Реалізує інтерфейс [MongoDB\\BSON\\ObjectIdInterface](class.mongodb-bson-objectidinterface.md)

| | PECL mongodb 1.2.0 Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md).

## Зміст

-   [MongoDB\\BSON\\ObjectId::\_\_construct](mongodb-bson-objectid.construct.md) \- Створює новий ObjectId
-   [MongoDB\\BSON\\ObjectId::getTimestamp](mongodb-bson-objectid.gettimestamp.md)— Повертає позначку часу ObjectId
-   [MongoDB\\BSON\\ObjectId::jsonSerialize](mongodb-bson-objectid.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\ObjectId::serialize](mongodb-bson-objectid.serialize.md) \- Серіалізує ObjectId
-   [MongoDB\\BSON\\ObjectId::\_\_function toString() { \[native code\] }](mongodb-bson-objectid.tostring.md)— Повертає шістнадцяткову виставу ObjectId
-   [MongoDB\\BSON\\ObjectId::unserialize](mongodb-bson-objectid.unserialize.md) \- Десеріалізує ObjectId
