Клас MongoDBDriverWriteResult

-   [« MongoDB\\Driver\\WriteError::getMessage](mongodb-driver-writeerror.getmessage.html)
    
-   [MongoDB\\Driver\\WriteResult::getDeletedCount »](mongodb-driver-writeresult.getdeletedcount.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver](book.mongodb.html)
    
-   Клас MongoDBDriverWriteResult
    

# Клас MongoDBDriverWriteResult

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteResult** інкапсулює інформацію про виконане [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html) і може бути повернутий [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html)

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\WriteResult
     
     {


    /* Методы */
    
   final public getDeletedCount(): ?int
final public getInsertedCount(): ?int
final public getMatchedCount(): ?int
final public getModifiedCount(): ?int
final public getServer(): MongoDB\Driver\Server
final public getUpsertedCount(): ?int
final public getUpsertedIds(): array
final public getWriteConcernError(): ?MongoDB\Driver\WriteConcernError
final public getWriteErrors(): array
final public isAcknowledged(): bool

   }
```

## Зміст

-   [MongoDB\\Driver\\WriteResult::getDeletedCount](mongodb-driver-writeresult.getdeletedcount.html) — Повертає кількість видалених документів
-   [MongoDB\\Driver\\WriteResult::getInsertedCount](mongodb-driver-writeresult.getinsertedcount.html) — Повертає кількість вставлених документів (за винятком злиття)
-   [MongoDB\\Driver\\WriteResult::getMatchedCount](mongodb-driver-writeresult.getmatchedcount.html) — Повертає кількість вибраних документів для оновлення
-   [MongoDB\\Driver\\WriteResult::getModifiedCount](mongodb-driver-writeresult.getmodifiedcount.html) — Повертає кількість існуючих оновлених документів
-   [MongoDB\\Driver\\WriteResult::getServer](mongodb-driver-writeresult.getserver.html) — Повертає сервер, пов'язаний із цим результатом запису
-   [MongoDB\\Driver\\WriteResult::getUpsertedCount](mongodb-driver-writeresult.getupsertedcount.html) — Повертає кількість документів, вставлених злиттям
-   [MongoDB\\Driver\\WriteResult::getUpsertedIds](mongodb-driver-writeresult.getupsertedids.html) — Повертає масив ідентифікаторів для об'єднаних документів
-   [MongoDB\\Driver\\WriteResult::getWriteConcernError](mongodb-driver-writeresult.getwriteconcernerror.html) — Повертає будь-яку помилку гарантій запису, що відбувся
-   [MongoDB\\Driver\\WriteResult::getWriteErrors](mongodb-driver-writeresult.getwriteerrors.html) — Повертає будь-які помилки запису, що сталися
-   [MongoDB\\Driver\\WriteResult::isAcknowledged](mongodb-driver-writeresult.isacknowledged.html) — Повертає, чи був запис підтверджений