---
navigation:
  - mongodb-driver-writeconcernerror.getmessage.md: '« MongoDBDriverWriteConcernError::getMessage'
  - mongodb-driver-writeerror.getcode.md: 'MongoDBDriverWriteError::getCode »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverWriteError
---
# Клас MongoDBDriverWriteError

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteError** інкапсулює інформацію про помилку запису і може бути повернутий як елемент масиву з [MongoDBDriverWriteResult::getWriteErrors()](mongodb-driver-writeresult.getwriteerrors.md)

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

-   [MongoDBDriverWriteError::getCode](mongodb-driver-writeerror.getcode.md) — Повертає код помилки WriteError
-   [MongoDBDriverWriteError::getIndex](mongodb-driver-writeerror.getindex.md) — Повертає індекс запису, який відповідає цьому WriteError
-   [MongoDBDriverWriteError::getInfo](mongodb-driver-writeerror.getinfo.md) — Повертає документ метаданих для WriteError
-   [MongoDBDriverWriteError::getMessage](mongodb-driver-writeerror.getmessage.md) — Повертає повідомлення про помилку WriteError
