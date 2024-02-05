---
navigation:
  - mongodb-driver-bulkwrite.update.md: '« MongoDB\\Driver\\BulkWrite::update'
  - mongodb-driver-session.aborttransaction.md: 'MongoDB\\Driver\\Session::abortTransaction »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\Session
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Session

(mongodb >=1.4.0)

## Вступ

Класс**MongoDB\\Driver\\Session** представляє клієнтський сеанс та повертається [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md). Команди, запити та операції запису можуть бути пов'язані з сеансом.

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

-   [MongoDB\\Driver\\Session::abortTransaction](mongodb-driver-session.aborttransaction.md)— Перериває транзакцію
-   [MongoDB\\Driver\\Session::advanceClusterTime](mongodb-driver-session.advanceclustertime.md) \- Збільшує час кластера для сеансу
-   [MongoDB\\Driver\\Session::advanceOperationTime](mongodb-driver-session.advanceoperationtime.md) \- Збільшує час операції для сеансу
-   [MongoDB\\Driver\\Session::commitTransaction](mongodb-driver-session.committransaction.md) \- Фіксує транзакцію
-   [MongoDB\\Driver\\Session::\_\_construct](mongodb-driver-session.construct.md)— Створює новий сеанс (не використовується)
-   [MongoDB\\Driver\\Session::endSession](mongodb-driver-session.endsession.md) \- Завершує сеанс
-   [MongoDB\\Driver\\Session::getClusterTime](mongodb-driver-session.getclustertime.md)— Повертає час кластера для цього сеансу
-   [MongoDB\\Driver\\Session::getLogicalSessionId](mongodb-driver-session.getlogicalsessionid.md)— Повертає логічний ідентифікатор сеансу для цього сеансу
-   [MongoDB\\Driver\\Session::getOperationTime](mongodb-driver-session.getoperationtime.md)— Повертає час операції для цього сеансу
-   [MongoDB\\Driver\\Session::getServer](mongodb-driver-session.getserver.md)— Повертає сервер, до якого прив'язана поточна сесія.
-   [MongoDB\\Driver\\Session::getTransactionOptions](mongodb-driver-session.gettransactionoptions.md)— Повертає налаштування поточної транзакції
-   [MongoDB\\Driver\\Session::getTransactionState](mongodb-driver-session.gettransactionstate.md)— Повертає статус транзакції для поточної сесії
-   [MongoDB\\Driver\\Session::isDirty](mongodb-driver-session.isdirty.md)— Повертає, чи сесія була позначена як брудна
-   [MongoDB\\Driver\\Session::isInTransaction](mongodb-driver-session.isintransaction.md)— Визначає, чи відбувається зараз багатодокументна транзакція.
-   [MongoDB\\Driver\\Session::startTransaction](mongodb-driver-session.starttransaction.md) \- Запускає транзакцію
