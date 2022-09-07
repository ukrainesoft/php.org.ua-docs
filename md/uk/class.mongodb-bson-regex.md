---
navigation:
  - mongodb-bson-objectid.unserialize.md: '« MongoDBBSONObjectId::unserialize'
  - mongodb-bson-regex.construct.md: 'MongoDBBSONRegex::construct »'
  - index.md: PHP Manual
  - book.bson.md: MongoDBBSON
title: Клас MongoDBBSONRegex
---
# Клас MongoDBBSONRegex

(mongodb >=1.0.0)

## Вступ

Тип BSON для шаблону регулярного вираження та додаткові [» флаги](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)

> **Зауваження**: Цей тип BSON в основному використовується при запитах до бази даних. Як альтернативу можна використовувати оператор запиту [» $regex](https://www.mongodb.com/docs/manual/reference/operator/query/regex)

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
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.md) для PHP 8.0+. |
| PECL mongodb 1.3.0 | Реалізує інтерфейс [MongoDBBSONRegexInterface](class.mongodb-bson-regexinterface.md) |
| PECL mongodb 1.2.0 | Реалізує інтерфейси [Serializable](class.serializable.md) і [JsonSerializable](class.jsonserializable.md) |

## Зміст

-   [MongoDBBSONRegex::construct](mongodb-bson-regex.construct.md) - Створює новий Regex
-   [MongoDBBSONRegex::getFlags](mongodb-bson-regex.getflags.md) — Повертає прапори Regex
-   [MongoDBBSONRegex::getPattern](mongodb-bson-regex.getpattern.md) — Повертає шаблон Regex
-   [MongoDBBSONRegex::jsonSerialize](mongodb-bson-regex.jsonserialize.md) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDBBSONRegex::serialize](mongodb-bson-regex.serialize.md) - Серіалізує Regex
-   [MongoDBBSONRegex::toString](mongodb-bson-regex.tostring.md) — Повертає рядкову виставу Regex
-   [MongoDBBSONRegex::unserialize](mongodb-bson-regex.unserialize.md) - Десеріалізує Regex
