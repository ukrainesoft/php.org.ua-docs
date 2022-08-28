Клас MongoDBDriverSession

-   [« MongoDB\\Driver\\BulkWrite::update](mongodb-driver-bulkwrite.update.html)
    
-   [MongoDB\\Driver\\Session::abortTransaction »](mongodb-driver-session.aborttransaction.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver](book.mongodb.html)
    
-   Клас MongoDBDriverSession
    

# Клас MongoDBDriverSession

(mongodb >=1.4.0)

## Вступ

Клас **MongoDBDriverSession** представляє клієнтський сеанс та повертається [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.html). Команди, запити та операції запису можуть бути пов'язані з сеансом.

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

-   [MongoDB\\Driver\\Session::abortTransaction](mongodb-driver-session.aborttransaction.html) — Перериває транзакцію
-   [MongoDB\\Driver\\Session::advanceClusterTime](mongodb-driver-session.advanceclustertime.html) - Збільшує час кластера для сеансу
-   [MongoDB\\Driver\\Session::advanceOperationTime](mongodb-driver-session.advanceoperationtime.html) - Збільшує час операції для сеансу
-   [MongoDB\\Driver\\Session::commitTransaction](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [MongoDB\\Driver\\Session::\_\_construct](mongodb-driver-session.construct.html) — Створює новий сеанс (не використовується)
-   [MongoDB\\Driver\\Session::endSession](mongodb-driver-session.endsession.html) - Завершує сеанс
-   [MongoDB\\Driver\\Session::getClusterTime](mongodb-driver-session.getclustertime.html) — Повертає час кластера для цього сеансу
-   [MongoDB\\Driver\\Session::getLogicalSessionId](mongodb-driver-session.getlogicalsessionid.html) — Повертає логічний ідентифікатор сеансу для цього сеансу
-   [MongoDB\\Driver\\Session::getOperationTime](mongodb-driver-session.getoperationtime.html) — Повертає час операції для цього сеансу
-   [MongoDB\\Driver\\Session::getServer](mongodb-driver-session.getserver.html) — Повертає сервер, до якого прив'язана поточна сесія.
-   [MongoDB\\Driver\\Session::getTransactionOptions](mongodb-driver-session.gettransactionoptions.html) — Повертає налаштування поточної транзакції
-   [MongoDB\\Driver\\Session::getTransactionState](mongodb-driver-session.gettransactionstate.html) — Повертає статус транзакції для поточної сесії
-   [MongoDB\\Driver\\Session::isDirty](mongodb-driver-session.isdirty.html) — Повертає, чи сесія була позначена як брудна
-   [MongoDB\\Driver\\Session::isInTransaction](mongodb-driver-session.isintransaction.html) — Визначає, чи відбувається зараз багатодокументна транзакція.
-   [MongoDB\\Driver\\Session::startTransaction](mongodb-driver-session.starttransaction.html) - Запускає транзакцію