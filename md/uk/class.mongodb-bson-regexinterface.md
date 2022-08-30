Інтерфейс MongoDBBSONRegexInterface

-   [« MongoDBBSONObjectIdInterface::toString](mongodb-bson-objectidinterface.tostring.html)
    
-   [MongoDBBSONRegexInterface::getFlags »](mongodb-bson-regexinterface.getflags.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBBSON](book.bson.md)
    
-   Інтерфейс MongoDBBSONRegexInterface
    

# Інтерфейс MongoDBBSONRegexInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDBBSONRegex](class.mongodb-bson-regex.html), як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

## Огляд класів

```classsynopsis

    
     
      class MongoDB\BSON\RegexInterface
     
     {
    /* Методы */
    
   abstract public getFlags(): string
abstract public getPattern(): string
abstract public __toString(): string

   }
```

## список змін

| Версия              | Описание                                                                                                                                                                                                                                                                                                                |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDBBSONRegexInterface::getFlags](mongodb-bson-regexinterface.getflags.html) — Повертає прапори RegexInterface
-   [MongoDBBSONRegexInterface::getPattern](mongodb-bson-regexinterface.getpattern.html) — Повертає шаблон RegexInterface
-   [MongoDBBSONRegexInterface::toString](mongodb-bson-regexinterface.tostring.html) — Повертає рядкову виставу RegexInterface