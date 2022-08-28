Інтерфейс MongoDBBSONRegexInterface

-   [« MongoDB\\BSON\\ObjectIdInterface::\_\_toString](mongodb-bson-objectidinterface.tostring.html)
    
-   [MongoDB\\BSON\\RegexInterface::getFlags »](mongodb-bson-regexinterface.getflags.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON](book.bson.html)
    
-   Інтерфейс MongoDBBSONRegexInterface
    

# Інтерфейс MongoDBBSONRegexInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html), як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

-   [MongoDB\\BSON\\RegexInterface::getFlags](mongodb-bson-regexinterface.getflags.html) — Повертає прапори RegexInterface
-   [MongoDB\\BSON\\RegexInterface::getPattern](mongodb-bson-regexinterface.getpattern.html) — Повертає шаблон RegexInterface
-   [MongoDB\\BSON\\RegexInterface::\_\_toString](mongodb-bson-regexinterface.tostring.html) — Повертає рядкову виставу RegexInterface