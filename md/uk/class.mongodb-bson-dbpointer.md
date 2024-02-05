---
navigation:
  - mongodb-bson-utcdatetimeinterface.tostring.md: >-
      « MongoDB\\BSON\\UTCDateTimeInterface::\_\_function toString() { [native
      code] }
  - mongodb-bson-dbpointer.construct.md: 'MongoDB\\BSON\\DBPointer::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\DBPointer (застарілий)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\DBPointer (застарілий)

(mongodb >=1.4.0)

## Вступ

Тип BSON типу "DBPointer". Цей тип BSON застарів і цей клас не може бути створений. Він буде створений з типу BSON DBPointer під час перетворення BSON на PHP, а також при перетворенні назад у BSON при зберіганні документів у базі даних.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\BSON\DBPointer
     

     implements 
       MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {
    

    /* Методы */
    
   final private __construct()
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

## Зміст

-   [MongoDB\\BSON\\DBPointer::\_\_construct](mongodb-bson-dbpointer.construct.md)— Створює новий DBPointer (не використовується)
-   [MongoDB\\BSON\\DBPointer::jsonSerialize](mongodb-bson-dbpointer.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\DBPointer::serialize](mongodb-bson-dbpointer.serialize.md) \- Серіалізує DBPointer
-   [MongoDB\\BSON\\DBPointer::\_\_function toString() { \[native code\] }](mongodb-bson-dbpointer.tostring.md)— Повертає порожній рядок
-   [MongoDB\\BSON\\DBPointer::unserialize](mongodb-bson-dbpointer.unserialize.md) \- Десеріалізує DBPointer
