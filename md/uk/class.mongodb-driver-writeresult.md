---
navigation:
  - mongodb-driver-writeerror.getmessage.html: '« MongoDBDriverWriteError::getMessage'
  - mongodb-driver-writeresult.getdeletedcount.html: 'MongoDBDriverWriteResult::getDeletedCount »'
  - index.html: PHP Manual
  - book.mongodb.html: MongoDBDriver
title: Клас MongoDBDriverWriteResult
---
# Клас MongoDBDriverWriteResult

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteResult** інкапсулює інформацію про виконане [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html) і може бути повернутий [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html)

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

-   [MongoDBDriverWriteResult::getDeletedCount](mongodb-driver-writeresult.getdeletedcount.html) — Повертає кількість видалених документів
-   [MongoDBDriverWriteResult::getInsertedCount](mongodb-driver-writeresult.getinsertedcount.html) — Повертає кількість вставлених документів (за винятком злиття)
-   [MongoDBDriverWriteResult::getMatchedCount](mongodb-driver-writeresult.getmatchedcount.html) — Повертає кількість вибраних документів для оновлення
-   [MongoDBDriverWriteResult::getModifiedCount](mongodb-driver-writeresult.getmodifiedcount.html) — Повертає кількість існуючих оновлених документів
-   [MongoDBDriverWriteResult::getServer](mongodb-driver-writeresult.getserver.html) — Повертає сервер, пов'язаний із цим результатом запису
-   [MongoDBDriverWriteResult::getUpsertedCount](mongodb-driver-writeresult.getupsertedcount.html) — Повертає кількість документів, вставлених злиттям
-   [MongoDBDriverWriteResult::getUpsertedIds](mongodb-driver-writeresult.getupsertedids.html) — Повертає масив ідентифікаторів для об'єднаних документів
-   [MongoDBDriverWriteResult::getWriteConcernError](mongodb-driver-writeresult.getwriteconcernerror.html) — Повертає будь-яку помилку гарантій запису, що відбувся
-   [MongoDBDriverWriteResult::getWriteErrors](mongodb-driver-writeresult.getwriteerrors.html) — Повертає будь-які помилки запису, що сталися
-   [MongoDBDriverWriteResult::isAcknowledged](mongodb-driver-writeresult.isacknowledged.html) — Повертає, чи був запис підтверджений
