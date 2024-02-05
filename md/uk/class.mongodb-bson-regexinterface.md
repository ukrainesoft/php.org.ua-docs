---
navigation:
  - mongodb-bson-objectidinterface.tostring.md: >-
      « MongoDB\\BSON\\ObjectIdInterface::\_\_function toString() { [native
      code] }
  - mongodb-bson-regexinterface.getflags.md: 'MongoDB\\BSON\\RegexInterface::getFlags »'
  - index.md: PHP Manual
  - book.bson.md: MongoDB\\BSON
title: Інтерфейс MongoDB\\BSON\\RegexInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\BSON\\RegexInterface

(mongodb >=1.3.0)

## Вступ

Цей інтерфейс реалізовано [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.md), як параметр, значення, що повертається або типу властивості в класах користувальницького простору.

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

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.15.0 | Типи значень, що повертаються для методів оголошені як попередні в PHP 8.0 і новіше, що викликає повідомлення про старіння в коді, який реалізує цей інтерфейс без оголошення відповідних типів значень, що повертаються. Атрибут `#[ReturnTypeWillChange]` може бути доданий, щоб заглушити повідомлення про старіння. |

## Зміст

-   [MongoDB\\BSON\\RegexInterface::getFlags](mongodb-bson-regexinterface.getflags.md)— Повертає прапори RegexInterface
-   [MongoDB\\BSON\\RegexInterface::getPattern](mongodb-bson-regexinterface.getpattern.md)— Повертає шаблон RegexInterface
-   [MongoDB\\BSON\\RegexInterface::\_\_function toString() { \[native code\] }](mongodb-bson-regexinterface.tostring.md)— Повертає рядкову виставу RegexInterface
