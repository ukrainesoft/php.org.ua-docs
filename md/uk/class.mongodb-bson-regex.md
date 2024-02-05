---
navigation:
  - mongodb-bson-objectid.unserialize.md: '« MongoDB\\BSON\\ObjectId::unserialize'
  - mongodb-bson-regex.construct.md: 'MongoDB\\BSON\\Regex::\_\_construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Клас MongoDB\\BSON\\Regex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\BSON\\Regex

(mongodb >=1.0.0)

## Вступ

Тип BSON для шаблону регулярного вираження та додаткові [»прапори](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)

> **Зауваження**: Цей тип BSON в основному використовується при запитах до бази даних. Як альтернативу можна використовувати оператор запиту [» $regex](https://www.mongodb.com/docs/manual/reference/operator/query/regex)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\BSON\Regex
     

     implements 
       MongoDB\BSON\RegexInterface,  MongoDB\BSON\Type,  Serializable,  JsonSerializable,  Stringable {


    /* Методы */
    
   final public __construct(string $pattern, string $flags = "")
final public getFlags(): string
final public getPattern(): string
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
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDB\\BSON\\RegexInterface](class.mongodb-bson-regexinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDB\\BSON\\Regex::\_\_construct](mongodb-bson-regex.construct.md) \- Створює новий Regex
-   [MongoDB\\BSON\\Regex::getFlags](mongodb-bson-regex.getflags.md)— Повертає прапори Regex
-   [MongoDB\\BSON\\Regex::getPattern](mongodb-bson-regex.getpattern.md)— Повертає шаблон Regex
-   [MongoDB\\BSON\\Regex::jsonSerialize](mongodb-bson-regex.jsonserialize.md)— Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Regex::serialize](mongodb-bson-regex.serialize.md) \- Серіалізує Regex
-   [MongoDB\\BSON\\Regex::\_\_function toString() { \[native code\] }](mongodb-bson-regex.tostring.md)— Повертає рядкову виставу Regex
-   [MongoDB\\BSON\\Regex::unserialize](mongodb-bson-regex.unserialize.md) \- Десеріалізує Regex
