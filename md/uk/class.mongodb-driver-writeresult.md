---
navigation:
  - mongodb-driver-writeerror.getmessage.md: '« MongoDBDriverWriteError::getMessage'
  - mongodb-driver-writeresult.getdeletedcount.md: 'MongoDBDriverWriteResult::getDeletedCount »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverWriteResult
---
# Клас MongoDBDriverWriteResult

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverWriteResult** інкапсулює інформацію про виконане [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md) і може бути повернутий [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)

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

-   [MongoDBDriverWriteResult::getDeletedCount](mongodb-driver-writeresult.getdeletedcount.md) — Повертає кількість видалених документів
-   [MongoDBDriverWriteResult::getInsertedCount](mongodb-driver-writeresult.getinsertedcount.md) — Повертає кількість вставлених документів (за винятком злиття)
-   [MongoDBDriverWriteResult::getMatchedCount](mongodb-driver-writeresult.getmatchedcount.md) — Повертає кількість вибраних документів для оновлення
-   [MongoDBDriverWriteResult::getModifiedCount](mongodb-driver-writeresult.getmodifiedcount.md) — Повертає кількість існуючих оновлених документів
-   [MongoDBDriverWriteResult::getServer](mongodb-driver-writeresult.getserver.md) — Повертає сервер, пов'язаний із цим результатом запису
-   [MongoDBDriverWriteResult::getUpsertedCount](mongodb-driver-writeresult.getupsertedcount.md) — Повертає кількість документів, вставлених злиттям
-   [MongoDBDriverWriteResult::getUpsertedIds](mongodb-driver-writeresult.getupsertedids.md) — Повертає масив ідентифікаторів для об'єднаних документів
-   [MongoDBDriverWriteResult::getWriteConcernError](mongodb-driver-writeresult.getwriteconcernerror.md) — Повертає будь-яку помилку гарантій запису, що відбувся
-   [MongoDBDriverWriteResult::getWriteErrors](mongodb-driver-writeresult.getwriteerrors.md) — Повертає будь-які помилки запису, що сталися
-   [MongoDBDriverWriteResult::isAcknowledged](mongodb-driver-writeresult.isacknowledged.md) — Повертає, чи був запис підтверджений
