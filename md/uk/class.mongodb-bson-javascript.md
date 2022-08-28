Клас MongoDBBSONJavascript

-   [« MongoDB\\BSON\\Decimal128::unserialize](mongodb-bson-decimal128.unserialize.html)
    
-   [MongoDB\\BSON\\Javascript::\_\_construct »](mongodb-bson-javascript.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Клас MongoDBBSONJavascript
    

# Клас MongoDBBSONJavascript

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
final public unserialize(string $serialized): void

   }
```

## список змін

| Версия              | Описание                                                                                                      |
|---------------------|---------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.12.0 | Реалізує інтерфейс [Stringable](class.stringable.html) для PHP 8.0+.                                          |
| PECL mongodb 1.3.0  | Реалізує інтерфейс [MongoDB\\BSON\\JavascriptInterface](class.mongodb-bson-javascriptinterface.html)          |
| PECL mongodb 1.2.0  | Реалізує інтерфейси [Serializable](class.serializable.html) і [JsonSerializable](class.jsonserializable.html) |

## Зміст

-   [MongoDB\\BSON\\Javascript::\_\_construct](mongodb-bson-javascript.construct.html) - Конструктор Javascript
-   [MongoDB\\BSON\\Javascript::getCode](mongodb-bson-javascript.getcode.html) — Повертає код JavaScript
-   [MongoDB\\BSON\\Javascript::getScope](mongodb-bson-javascript.getscope.html) — Повертає область документа JavaScript
-   [MongoDB\\BSON\\Javascript::jsonSerialize](mongodb-bson-javascript.jsonserialize.html) — Повертає виставу, яка може бути перетворена на JSON
-   [MongoDB\\BSON\\Javascript::serialize](mongodb-bson-javascript.serialize.html) — Серіалізувати JavaScript
-   [MongoDB\\BSON\\Javascript::\_\_toString](mongodb-bson-javascript.tostring.html) — Повертає код JavaScript
-   [MongoDB\\BSON\\Javascript::unserialize](mongodb-bson-javascript.unserialize.html) — Десеріалізувати JavaScript