---
navigation:
  - mongodb-driver-writeconcernerror.getmessage.html: '« MongoDBDriverWriteConcernError::getMessage'
  - mongodb-driver-writeerror.getcode.html: 'MongoDBDriverWriteError::getCode »'
  - index.html: PHP Manual
  - book.mongodb.html: MongoDBDriver
title: Клас MongoDBDriverWriteError
---
# Клас MongoDBDriverWriteError

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteError** інкапсулює інформацію про помилку запису і може бути повернутий як елемент масиву з [MongoDBDriverWriteResult::getWriteErrors()](mongodb-driver-writeresult.getwriteerrors.html)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\WriteError
     
     {


    /* Методы */
    
   final public getCode(): int
final public getIndex(): int
final public getInfo(): ?object
final public getMessage(): string

   }
```

## Зміст

-   [MongoDBDriverWriteError::getCode](mongodb-driver-writeerror.getcode.html) — Повертає код помилки WriteError
-   [MongoDBDriverWriteError::getIndex](mongodb-driver-writeerror.getindex.html) — Повертає індекс запису, який відповідає цьому WriteError
-   [MongoDBDriverWriteError::getInfo](mongodb-driver-writeerror.getinfo.html) — Повертає документ метаданих для WriteError
-   [MongoDBDriverWriteError::getMessage](mongodb-driver-writeerror.getmessage.html) — Повертає повідомлення про помилку WriteError
