---
navigation:
  - mongodb-bson-int64.unserialize.md: '« MongoDB\\BSON\\Int64::unserialize'
  - mongodb-bson-symbol.construct.md: 'MongoDB\\BSON\\Symbol::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Symbol (застарілий)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Symbol (застарілий)

(mongodb >=1.4.0)

## Вступ

Тип BSON типу "Symbol". Цей тип BSON застарів і цей клас не може бути створений. Він буде створений з типу символу BSON під час перетворення BSON на PHP, а також при перетворенні назад на BSON при зберіганні документів у базі даних.

## Огляд класів

```classsynopsis


    
    
     
      class MongoDB\BSON\Symbol
     

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

-   [MongoDB\\BSON\\Symbol::\_\_construct](mongodb-bson-symbol.construct.md)— Створює новий Symbol (не використовується)
-   [MongoDB\\BSON\\Symbol::jsonSerialize](mongodb-bson-symbol.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Symbol::serialize](mongodb-bson-symbol.serialize.md) \- Серіалізує Symbol
-   [MongoDB\\BSON\\Symbol::\_\_function toString() { \[native code\] }](mongodb-bson-symbol.tostring.md)— Повертає Symbol у вигляді рядка
-   [MongoDB\\BSON\\Symbol::unserialize](mongodb-bson-symbol.unserialize.md) \- Десеріалізує Symbol
