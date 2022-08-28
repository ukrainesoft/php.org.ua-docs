Клас The MongoDBDriverWriteConcernError

-   [« MongoDB\\Driver\\TopologyDescription::hasWritableServer](mongodb-driver-topologydescription.haswritableserver.html)
    
-   [MongoDB\\Driver\\WriteConcernError::getCode »](mongodb-driver-writeconcernerror.getcode.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver](book.mongodb.html)
    
-   Клас The MongoDBDriverWriteConcernError
    

# Клас The MongoDBDriverWriteConcernError

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteConcernError** інкапсулює інформацію про помилку запису і може бути повернутий [MongoDB\\Driver\\WriteResult::getWriteConcernError()](mongodb-driver-writeresult.getwriteconcernerror.html)

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

-   [MongoDB\\Driver\\WriteConcernError::getCode](mongodb-driver-writeconcernerror.getcode.html) — Повертає код помилки WriteConcernError
-   [MongoDB\\Driver\\WriteConcernError::getInfo](mongodb-driver-writeconcernerror.getinfo.html) — Повертає документ метаданих для WriteConcernError
-   [MongoDB\\Driver\\WriteConcernError::getMessage](mongodb-driver-writeconcernerror.getmessage.html) — Повертає повідомлення про помилку WriteConcernError