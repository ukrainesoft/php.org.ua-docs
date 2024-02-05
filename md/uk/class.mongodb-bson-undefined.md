---
navigation:
  - mongodb-bson-symbol.unserialize.md: '« MongoDB\\BSON\\Symbol::unserialize'
  - mongodb-bson-undefined.construct.md: 'MongoDB\\BSON\\Undefined::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Undefined (застаріло)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Undefined (застаріло)

(mongodb >=1.4.0)

## Вступ

Тип BSON типу "Undefined". Цей тип BSON застарів і цей клас не може бути створений. Він буде створений з невизначеного типу BSON під час перетворення BSON на PHP, а також може бути перетворений назад на BSON під час зберігання документів у базі даних.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\Undefined
     

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

-   [MongoDB\\BSON\\Undefined::\_\_construct](mongodb-bson-undefined.construct.md) \- Створює новий Undefined (не використовується)
-   [MongoDB\\BSON\\Undefined::jsonSerialize](mongodb-bson-undefined.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Undefined::serialize](mongodb-bson-undefined.serialize.md) \- Серіалізує Undefined
-   [MongoDB\\BSON\\Undefined::\_\_function toString() { \[native code\] }](mongodb-bson-undefined.tostring.md)— Повертає порожній рядок
-   [MongoDB\\BSON\\Undefined::unserialize](mongodb-bson-undefined.unserialize.md) \- Десеріалізує Undefined
