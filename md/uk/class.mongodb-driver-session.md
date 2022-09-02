---
navigation:
  - mongodb-driver-bulkwrite.update.md: '« MongoDBDriverBulkWrite::update'
  - mongodb-driver-session.aborttransaction.md: 'MongoDBDriverSession::abortTransaction »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverSession
---
# Клас MongoDBDriverSession

(mongodb >=1.4.0)

## Вступ

Клас **MongoDBDriverSession** представляє клієнтський сеанс та повертається [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.md). Команди, запити та операції запису можуть бути пов'язані з сеансом.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Session
     
     {


    /* Константы */
    
     const
     string
      TRANSACTION_NONE = none;

    const
     string
      TRANSACTION_STARTING = starting;

    const
     string
      TRANSACTION_IN_PROGRESS = in_progress;

    const
     string
      TRANSACTION_COMMITTED = committed;

    const
     string
      TRANSACTION_ABORTED = aborted;


    /* Методы */
    
   final public abortTransaction(): void
final public advanceClusterTime(array|object $clusterTime): void
final public advanceOperationTime(MongoDB\BSON\TimestampInterface $operationTime): void
final public commitTransaction(): void
final private __construct()
final public endSession(): void
final public getClusterTime(): ?object
final public getLogicalSessionId(): object
final public getOperationTime(): ?MongoDB\BSON\Timestamp
final public getServer(): ?MongoDB\Driver\Server
final public getTransactionOptions(): ?array
final public getTransactionState(): string
final public isDirty(): bool
final public isInTransaction(): boolean
final public startTransaction(?array $options = null): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\Session::TRANSACTION_NONE`**

Немає транзакції у процесі.

**`MongoDB\Driver\Session::TRANSACTION_STARTING`**

Транзакцію було розпочато, але на сервер не було надіслано жодної операції.

**`MongoDB\Driver\Session::TRANSACTION_IN_PROGRESS`**

Транзакція у процесі.

**`MongoDB\Driver\Session::TRANSACTION_COMMITTED`**

Транзакцію було зафіксовано.

**`MongoDB\Driver\Session::TRANSACTION_ABORTED`**

Транзакцію було перервано.

## Зміст

-   [MongoDBDriverSession::abortTransaction](mongodb-driver-session.aborttransaction.md) — Перериває транзакцію
-   [MongoDBDriverSession::advanceClusterTime](mongodb-driver-session.advanceclustertime.md) - Збільшує час кластера для сеансу
-   [MongoDBDriverSession::advanceOperationTime](mongodb-driver-session.advanceoperationtime.md) - Збільшує час операції для сеансу
-   [MongoDBDriverSession::commitTransaction](mongodb-driver-session.committransaction.md) - Фіксує транзакцію
-   [MongoDBDriverSession::construct](mongodb-driver-session.construct.md) — Створює новий сеанс (не використовується)
-   [MongoDBDriverSession::endSession](mongodb-driver-session.endsession.md) - Завершує сеанс
-   [MongoDBDriverSession::getClusterTime](mongodb-driver-session.getclustertime.md) — Повертає час кластера для цього сеансу
-   [MongoDBDriverSession::getLogicalSessionId](mongodb-driver-session.getlogicalsessionid.md) — Повертає логічний ідентифікатор сеансу для цього сеансу
-   [MongoDBDriverSession::getOperationTime](mongodb-driver-session.getoperationtime.md) — Повертає час операції для цього сеансу
-   [MongoDBDriverSession::getServer](mongodb-driver-session.getserver.md) — Повертає сервер, до якого прив'язана поточна сесія.
-   [MongoDBDriverSession::getTransactionOptions](mongodb-driver-session.gettransactionoptions.md) — Повертає налаштування поточної транзакції
-   [MongoDBDriverSession::getTransactionState](mongodb-driver-session.gettransactionstate.md) — Повертає статус транзакції для поточної сесії
-   [MongoDBDriverSession::isDirty](mongodb-driver-session.isdirty.md) — Повертає, чи сесія була позначена як брудна
-   [MongoDBDriverSession::isInTransaction](mongodb-driver-session.isintransaction.md) — Визначає, чи відбувається зараз багатодокументна транзакція.
-   [MongoDBDriverSession::startTransaction](mongodb-driver-session.starttransaction.md) - Запускає транзакцію
