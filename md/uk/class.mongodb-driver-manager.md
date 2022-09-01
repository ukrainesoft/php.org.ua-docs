---
navigation:
  - book.mongodb.html: « MongoDBDriver
  - mongodb-driver-manager.addsubscriber.html: 'MongoDBDriverManager::addSubscriber »'
  - index.html: PHP Manual
  - book.mongodb.html: MongoDBDriver
title: Клас MongoDBDriverManager
---
# Клас MongoDBDriverManager

(mongodb >=1.0.0)

## Вступ

Клас **MongoDBDriverManager** є основною точкою входу модуль. Він відповідає за підтримку з'єднань з MongoDB (будь то автономний сервер, набір реплік або розподілений кластер).

Під час ініціалізації класу Manager не підключено до MongoDB. Це означає, що **MongoDBDriverManager** завжди може бути створений навіть якщо сервери MongoDB не працюють.

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

**Приклад #1 Простий приклад використання [MongoDBDriverManager::construct()](mongodb-driver-manager.construct.html)**

Виводить різну інформацію про **MongoDBDriverManager** за допомогою функції [vardump()](function.var-dump.html). Це може бути корисним для налагодження, щоб подивитися як драйвер бачить налаштування MongoDB і які опції використовуються.

```php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager);

?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [MongoDBDriverManager::addSubscriber](mongodb-driver-manager.addsubscriber.html) — Реєструє передплатника на подію моніторингу в даному об'єкті Manager
-   [MongoDBDriverManager::construct](mongodb-driver-manager.construct.html) - Створює новий Manager MongoDB
-   [MongoDBDriverManager::createClientEncryption](mongodb-driver-manager.createclientencryption.html) — Створення нового об'єкта ClientEncryption
-   [MongoDBDriverManager::executeBulkWrite](mongodb-driver-manager.executebulkwrite.html) — Виконує одну або кілька операцій запису
-   [MongoDBDriverManager::executeCommand](mongodb-driver-manager.executecommand.html) - Виконує команду бази даних
-   [MongoDBDriverManager::executeQuery](mongodb-driver-manager.executequery.html) — Виконує запит до бази даних
-   [MongoDBDriverManager::executeReadCommand](mongodb-driver-manager.executereadcommand.html) - Виконує команду бази даних, яка читає
-   [MongoDBDriverManager::executeReadWriteCommand](mongodb-driver-manager.executereadwritecommand.html) — Виконує команду бази даних, яка читає та пише
-   [MongoDBDriverManager::executeWriteCommand](mongodb-driver-manager.executewritecommand.html) - Виконує команду бази даних, яка пише
-   [MongoDBDriverManager::getEncryptedFieldsMap](mongodb-driver-manager.getencryptedfieldsmap.html) — Повертає опцію автоматичного шифрування encryptedFieldsMap для Manager
-   [MongoDBDriverManager::getReadConcern](mongodb-driver-manager.getreadconcern.html) — Повертає ReadConcern для Manager
-   [MongoDBDriverManager::getReadPreference](mongodb-driver-manager.getreadpreference.html) — Повертає ReadPreference для Manager
-   [MongoDBDriverManager::getServers](mongodb-driver-manager.getservers.html) — Повертає сервери, до яких підключено менеджера
-   [MongoDBDriverManager::getWriteConcern](mongodb-driver-manager.getwriteconcern.html) — Повертає WriteConcern для Manager
-   [MongoDBDriverManager::removeSubscriber](mongodb-driver-manager.removesubscriber.html) — Скасує реєстрацію передплатника на подію моніторингу на даному об'єкті Manager
-   [MongoDBDriverManager::selectServer](mongodb-driver-manager.selectserver.html) — Вибрати сервер, який відповідає перевагам читання
-   [MongoDBDriverManager::startSession](mongodb-driver-manager.startsession.html) — Запуск нового клієнтського сеансу для використання з цим клієнтом
