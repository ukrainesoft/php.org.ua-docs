---
navigation:
  - mongodb-driver-topologydescription.haswritableserver.md: '« MongoDB\\Driver\\TopologyDescription::hasWritableServer'
  - mongodb-driver-writeconcernerror.getcode.md: 'MongoDB\\Driver\\WriteConcernError::getCode »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас The MongoDB\\Driver\\WriteConcernError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас The MongoDB\\Driver\\WriteConcernError

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\WriteConcernError** інкапсулює інформацію про помилку запису і може бути повернутий [MongoDB\\Driver\\WriteResult::getWriteConcernError()](mongodb-driver-writeresult.getwriteconcernerror.md)

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

-   [MongoDB\\Driver\\WriteConcernError::getCode](mongodb-driver-writeconcernerror.getcode.md)— Повертає код помилки WriteConcernError
-   [MongoDB\\Driver\\WriteConcernError::getInfo](mongodb-driver-writeconcernerror.getinfo.md)— Повертає документ метаданих для WriteConcernError
-   [MongoDB\\Driver\\WriteConcernError::getMessage](mongodb-driver-writeconcernerror.getmessage.md)— Повертає повідомлення про помилку WriteConcernError
