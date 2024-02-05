---
navigation:
  - mongodb-driver-writeerror.getmessage.md: '« MongoDB\\Driver\\WriteError::getMessage'
  - mongodb-driver-writeresult.getdeletedcount.md: 'MongoDB\\Driver\\WriteResult::getDeletedCount »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\WriteResult
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\WriteResult

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\WriteResult** інкапсулює інформацію про виконане [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md) і може бути повернутий [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)

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

-   [MongoDB\\Driver\\WriteResult::getDeletedCount](mongodb-driver-writeresult.getdeletedcount.md)— Повертає кількість видалених документів
-   [MongoDB\\Driver\\WriteResult::getInsertedCount](mongodb-driver-writeresult.getinsertedcount.md)— Повертає кількість вставлених документів (за винятком злиття)
-   [MongoDB\\Driver\\WriteResult::getMatchedCount](mongodb-driver-writeresult.getmatchedcount.md)— Повертає кількість вибраних документів для оновлення
-   [MongoDB\\Driver\\WriteResult::getModifiedCount](mongodb-driver-writeresult.getmodifiedcount.md)— Повертає кількість існуючих оновлених документів
-   [MongoDB\\Driver\\WriteResult::getServer](mongodb-driver-writeresult.getserver.md)— Повертає сервер, пов'язаний із цим результатом запису
-   [MongoDB\\Driver\\WriteResult::getUpsertedCount](mongodb-driver-writeresult.getupsertedcount.md)— Повертає кількість документів, вставлених злиттям
-   [MongoDB\\Driver\\WriteResult::getUpsertedIds](mongodb-driver-writeresult.getupsertedids.md)— Повертає масив ідентифікаторів для об'єднаних документів
-   [MongoDB\\Driver\\WriteResult::getWriteConcernError](mongodb-driver-writeresult.getwriteconcernerror.md)— Повертає будь-яку помилку гарантій запису, що відбувся
-   [MongoDB\\Driver\\WriteResult::getWriteErrors](mongodb-driver-writeresult.getwriteerrors.md)— Повертає будь-які помилки запису, що сталися
-   [MongoDB\\Driver\\WriteResult::isAcknowledged](mongodb-driver-writeresult.isacknowledged.md)— Повертає, чи був запис підтверджений
