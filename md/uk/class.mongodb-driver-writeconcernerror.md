Клас The MongoDBDriverWriteConcernError

-   [« MongoDBDriverTopologyDescription::hasWritableServer](mongodb-driver-topologydescription.haswritableserver.html)
    
-   [MongoDBDriverWriteConcernError::getCode »](mongodb-driver-writeconcernerror.getcode.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriver](book.mongodb.md)
    
-   Клас The MongoDBDriverWriteConcernError
    

# Клас The MongoDBDriverWriteConcernError

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteConcernError** інкапсулює інформацію про помилку запису і може бути повернутий [MongoDBDriverWriteResult::getWriteConcernError()](mongodb-driver-writeresult.getwriteconcernerror.html)

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

-   [MongoDBDriverWriteConcernError::getCode](mongodb-driver-writeconcernerror.getcode.html) — Повертає код помилки WriteConcernError
-   [MongoDBDriverWriteConcernError::getInfo](mongodb-driver-writeconcernerror.getinfo.html) — Повертає документ метаданих для WriteConcernError
-   [MongoDBDriverWriteConcernError::getMessage](mongodb-driver-writeconcernerror.getmessage.html) — Повертає повідомлення про помилку WriteConcernError