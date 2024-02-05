---
navigation:
  - mongodb-bson-decimal128.unserialize.md: '« MongoDB\\BSON\\Decimal128::unserialize'
  - mongodb-bson-javascript.construct.md: 'MongoDB\\BSON\\Javascript::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Javascript
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Javascript

(mongodb >=1.0.0)

## Вступ

Тип BSON для Javascript. Може бути зазначений необов'язковий документ області видимості, який зіставляє ідентифікатори зі значеннями та визначає область, де код повинен оцінюватися сервером.

> **Зауваження**: Цей тип BSON в основному використовується при виконанні команд бази даних, які приймають функцію Javascript як параметр, наприклад [» mapReduce](https://www.mongodb.com/docs/manual/reference/command/mapReduce/)

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\BSON\Javascript
     

     implements 
       MongoDB\BSON\JavascriptInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {
    

    /* Методы */
    
   final public __construct(string $code, array|object|null $scope = null)
final public getCode(): string
final public getScope(): ?object
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
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\JavascriptInterface](class.mongodb-bson-javascriptinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\Javascript::\_\_construct](mongodb-bson-javascript.construct.md) \- Конструктор Javascript
-   [MongoDB\\BSON\\Javascript::getCode](mongodb-bson-javascript.getcode.md)— Повертає код JavaScript
-   [MongoDB\\BSON\\Javascript::getScope](mongodb-bson-javascript.getscope.md)— Повертає область документа JavaScript
-   [MongoDB\\BSON\\Javascript::jsonSerialize](mongodb-bson-javascript.jsonserialize.md)— Повертає виставу, яка може бути перетворена на JSON
-   [MongoDB\\BSON\\Javascript::serialize](mongodb-bson-javascript.serialize.md)— Серіалізувати JavaScript
-   [MongoDB\\BSON\\Javascript::\_\_function toString() { \[native code\] }](mongodb-bson-javascript.tostring.md)— Повертає код JavaScript
-   [MongoDB\\BSON\\Javascript::unserialize](mongodb-bson-javascript.unserialize.md)— Десеріалізувати JavaScript
