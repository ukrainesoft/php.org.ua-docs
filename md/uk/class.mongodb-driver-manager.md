---
navigation:
  - book.mongodb.md: « MongoDB\\Driver
  - mongodb-driver-manager.addsubscriber.md: 'MongoDB\\Driver\\Manager::addSubscriber »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\Manager
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Manager

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\Manager** є основною точкою входу модуль. Він відповідає за підтримку з'єднань з MongoDB (будь то автономний сервер, набір реплік або розподілений кластер).

Під час ініціалізації класу Manager не підключено до MongoDB. Це означає, що **MongoDB\\Driver\\Manager** завжди може бути створений навіть якщо сервери MongoDB не працюють.

Будь-який запис або запит будуть викидати виключення з'єднання, оскільки з'єднання створюються "ліниво" (на вимогу). Сервер MongoDB також може бути недоступним протягом усього часу скрипту. Тому важливо, щоб усі дії з Manager були загорнуті до блоку try/catch.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\Manager
     
     {


    /* Методы */
    
   final public addSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
final public __construct(?string $uri = null, ?array $uriOptions = null, ?array $driverOptions = null)
final public createClientEncryption(array $options): MongoDB\Driver\ClientEncryption
final public executeBulkWrite(string $namespace, MongoDB\Driver\BulkWrite $bulk, array|MongoDB\Driver\WriteConcern|null $options = null): MongoDB\Driver\WriteResult
final public executeCommand(string $db, MongoDB\Driver\Command $command, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
final public executeQuery(string $namespace, MongoDB\Driver\Query $query, array|MongoDB\Driver\ReadPreference|null $options = null): MongoDB\Driver\Cursor
final public executeReadCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
final public executeReadWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
final public executeWriteCommand(string $db, MongoDB\Driver\Command $command, ?array $options = null): MongoDB\Driver\Cursor
final public getEncryptedFieldsMap(): array|object|null
final public getReadConcern(): MongoDB\Driver\ReadConcern
final public getReadPreference(): MongoDB\Driver\ReadPreference
final public getServers(): array
final public getWriteConcern(): MongoDB\Driver\WriteConcern
final public removeSubscriber(MongoDB\Driver\Monitoring\Subscriber $subscriber): void
final public selectServer(?MongoDB\Driver\ReadPreference $readPreference = null): MongoDB\Driver\Server
final public startSession(?array $options = null): MongoDB\Driver\Session

   }
```

## Приклади

**Приклад #1 Простий приклад використання [MongoDB\\Driver\\Manager::\_\_construct()](mongodb-driver-manager.construct.md)**

Виводить різну інформацію про **MongoDB\\Driver\\Manager** за допомогою функції [var\_dump()](function.var-dump.md). Це може бути корисним для налагодження, щоб подивитися як драйвер бачить налаштування MongoDB і які опції використовуються.

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager);

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MongoDB\Driver\Manager)#1 (2) {
  ["uri"]=>
  string(26) "mongodb://127.0.0.1:27017/"
  ["cluster"]=>
  array(0) {
  }
}
```

## Зміст

-   [MongoDB\\Driver\\Manager::addSubscriber](mongodb-driver-manager.addsubscriber.md)— Реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDB\\Driver\\Manager::\_\_construct](mongodb-driver-manager.construct.md) \- Створює новий Manager MongoDB
-   [MongoDB\\Driver\\Manager::createClientEncryption](mongodb-driver-manager.createclientencryption.md)— Створення нового об'єкта ClientEncryption
-   [MongoDB\\Driver\\Manager::executeBulkWrite](mongodb-driver-manager.executebulkwrite.md)— Виконує одну або кілька операцій запису
-   [MongoDB\\Driver\\Manager::executeCommand](mongodb-driver-manager.executecommand.md) \- Виконує команду бази даних
-   [MongoDB\\Driver\\Manager::executeQuery](mongodb-driver-manager.executequery.md)— Виконує запит до бази даних
-   [MongoDB\\Driver\\Manager::executeReadCommand](mongodb-driver-manager.executereadcommand.md) \- Виконує команду бази даних, яка читає
-   [MongoDB\\Driver\\Manager::executeReadWriteCommand](mongodb-driver-manager.executereadwritecommand.md)— Виконує команду бази даних, яка читає та пише
-   [MongoDB\\Driver\\Manager::executeWriteCommand](mongodb-driver-manager.executewritecommand.md) \- Виконує команду бази даних, яка пише
-   [MongoDB\\Driver\\Manager::getEncryptedFieldsMap](mongodb-driver-manager.getencryptedfieldsmap.md)— Повертає опцію автоматичного шифрування encryptedFieldsMap для Manager
-   [MongoDB\\Driver\\Manager::getReadConcern](mongodb-driver-manager.getreadconcern.md)— Повертає ReadConcern для Manager
-   [MongoDB\\Driver\\Manager::getReadPreference](mongodb-driver-manager.getreadpreference.md)— Повертає ReadPreference для Manager
-   [MongoDB\\Driver\\Manager::getServers](mongodb-driver-manager.getservers.md)— Повертає сервери, до яких підключено менеджера
-   [MongoDB\\Driver\\Manager::getWriteConcern](mongodb-driver-manager.getwriteconcern.md)— Повертає WriteConcern для Manager
-   [MongoDB\\Driver\\Manager::removeSubscriber](mongodb-driver-manager.removesubscriber.md)— Скасує реєстрацію передплатника на подію моніторингу на даному об'єкті Manager
-   [MongoDB\\Driver\\Manager::selectServer](mongodb-driver-manager.selectserver.md)— Вибрати сервер, який відповідає перевагам читання
-   [MongoDB\\Driver\\Manager::startSession](mongodb-driver-manager.startsession.md)— Запуск нового клієнтського сеансу для використання з цим клієнтом
