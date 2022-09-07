---
navigation:
  - mongodb-driver-topologydescription.haswritableserver.md: '« MongoDBDriverTopologyDescription::hasWritableServer'
  - mongodb-driver-writeconcernerror.getcode.md: 'MongoDBDriverWriteConcernError::getCode »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас The MongoDBDriverWriteConcernError
---
# Клас The MongoDBDriverWriteConcernError

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteConcernError** інкапсулює інформацію про помилку запису і може бути повернутий [MongoDBDriverWriteResult::getWriteConcernError()](mongodb-driver-writeresult.getwriteconcernerror.md)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\WriteConcernError
     
     {


    /* Методы */
    
   final public getCode(): int
final public getInfo(): ?object
final public getMessage(): string

   }
```

## Зміст

-   [MongoDBDriverWriteConcernError::getCode](mongodb-driver-writeconcernerror.getcode.md) — Повертає код помилки WriteConcernError
-   [MongoDBDriverWriteConcernError::getInfo](mongodb-driver-writeconcernerror.getinfo.md) — Повертає документ метаданих для WriteConcernError
-   [MongoDBDriverWriteConcernError::getMessage](mongodb-driver-writeconcernerror.getmessage.md) — Повертає повідомлення про помилку WriteConcernError
