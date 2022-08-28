Клас MongoDBBSONRegex

-   [« MongoDB\\BSON\\ObjectId::unserialize](mongodb-bson-objectid.unserialize.html)
    
-   [MongoDB\\BSON\\Regex::\_\_construct »](mongodb-bson-regex.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Клас MongoDBBSONRegex
    

# Клас MongoDBBSONRegex

(mongodb >=1.0.0)

## Вступ

Тип BSON для шаблону регулярного вираження та додаткові [» флаги](https://www.mongodb.com/docs/manual/reference/operator/query/regex/#op._S_options)

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
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия              | Описание                                                                                                      |
|---------------------|---------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+.                                          |
| PECL mongodb 1.3.0  | Реалізує інтерфейс [MongoDB\\BSON\\RegexInterface](class.mongodb-bson-regexinterface.html)                    |
| PECL mongodb 1.2.0  | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDB\\BSON\\Regex::\_\_construct](mongodb-bson-regex.construct.html) - Створює новий Regex
-   [MongoDB\\BSON\\Regex::getFlags](mongodb-bson-regex.getflags.html) — Повертає прапори Regex
-   [MongoDB\\BSON\\Regex::getPattern](mongodb-bson-regex.getpattern.html) — Повертає шаблон Regex
-   [MongoDB\\BSON\\Regex::jsonSerialize](mongodb-bson-regex.jsonserialize.html) — Повертає уявлення, яке можна перетворити на JSON
-   [MongoDB\\BSON\\Regex::serialize](mongodb-bson-regex.serialize.html) - Серіалізує Regex
-   [MongoDB\\BSON\\Regex::\_\_toString](mongodb-bson-regex.tostring.html) — Повертає рядкову виставу Regex
-   [MongoDB\\BSON\\Regex::unserialize](mongodb-bson-regex.unserialize.html) - Десеріалізує Regex