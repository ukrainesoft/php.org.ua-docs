---
navigation:
  - mongodb-driver-manager.createclientencryption.md: '« MongoDB\\Driver\\Manager::createClientEncryption'
  - mongodb-driver-manager.executecommand.md: 'MongoDB\\Driver\\Manager::executeCommand »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::executeBulkWrite'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::executeBulkWrite

(mongodb >=1.0.0)

MongoDB\\Driver\\Manager::executeBulkWrite — Виконує одну або кілька операцій запису

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::executeBulkWrite(string $namespace, MongoDB\Driver\BulkWrite $bulk, array|MongoDB\Driver\WriteConcern|null $options = null): MongoDB\Driver\WriteResult
```

Виконує одну або кілька операцій запису на основному сервері.

Об'єкт класу [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md) може бути створений з однією або декількома операціями запису різного типу (наприклад, оновлення, видалення та вставки). Драйвер спробує надіслати операції одного і того ж типу на сервер з мінімальною кількістю запитів, щоб скоротити звернення до сервера.

### Список параметрів

`namespace`(string)

Повністю певне ім'я (тобто . `"databaseName.collectionName"`

`bulk` [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)) .

Записи для виконання.

`опції`

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| session | [MongoDB\\Driver\\Session](class.mongodb-driver-session.md) |  |
| Сесія зв'язування з операцією. |  |  |

| | writeConcern |[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

### Значення, що повертаються

У разі успішного виконання повертає [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)

### Помилки

-   За відсутності будь-якої операції запису в`bulk`, викидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Якщо `bulk`вже був виконаний, викидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md). Об'єкти[MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)не можуть бути виконані кілька разів.
-   Викидається [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опція `"session"`вказано у поєднанні з непідтвердженою гарантією запису.
-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   При помилці запису кидає виняток[MongoDB\\Driver\\Exception\\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md)
-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   При виникненні інших помилок викидає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.4.4 | Якщо опція `"session"` використовується у поєднанні з непідтвердженою гарантією запису, викидається виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) |
| PECL mongodb 1.4.0 | Третій параметр `options` тепер масив. Для зворотної сумісності цей параметр ще приймає об'єкт [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md) |
| PECL mongodb 1.3.0 | Тепер викидається виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md), якщо `bulk` не містить операцій запису. Раніше викидалося [MongoDB\\Driver\\Exception\\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.md) |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\Manager::executeBulkWrite()\*\*\*\*

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite();

$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);

$bulk->update(['x' => 2], ['$set' => ['x' => 1]], ['multi' => false, 'upsert' => false]);
$bulk->update(['x' => 3], ['$set' => ['x' => 3]], ['multi' => false, 'upsert' => true]);
$bulk->update(['_id' => 3], ['$set' => ['x' => 3]], ['multi' => false, 'upsert' => true]);

$bulk->insert(['_id' => 4, 'x' => 2]);

$bulk->delete(['x' => 1], ['limit' => 1]);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 100);
$result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);

printf("Добавлено %d документ(ов)\n", $result->getInsertedCount());
printf("Найдено %d документ(ов)\n", $result->getMatchedCount());
printf("Обновлено %d документ(ов)\n", $result->getModifiedCount());
printf("Добавлено и добавлено %d документ(ов)\n", $result->getUpsertedCount());
printf("Удалено %d документ(ов)\n", $result->getDeletedCount());

foreach ($result->getUpsertedIds() as $index => $id) {
    printf('upsertedId[%d]: ', $index);
    var_dump($id);
}

/* Если WriteConcern не может быть выполнен */
if ($writeConcernError = $result->getWriteConcernError()) {
    printf("%s (%d): %s\n", $writeConcernError->getMessage(), $writeConcernError->getCode(), var_export($writeConcernError->getInfo(), true));
}

/* Если запись не может произойти вообще*/
foreach ($result->getWriteErrors() as $writeError) {
    printf("Операция#%d: %s (%d)\n", $writeError->getIndex(), $writeError->getMessage(), $writeError->getCode());
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Добавлено 3 документ(ов)
Найдено 1 документ(ов)
Обновлено 1 документ(ов)
Добавлено и добавлено 2 документ(ов)
Удалено 1 документ(ов)
upsertedId[3]: object(MongoDB\BSON\ObjectId)#5 (1) {
  ["oid"]=>
  string(24) "54d3adc3ce7a792f4d703756"
}
upsertedId[4]: int(3)
```

### Дивіться також

-   [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)
-   [MongoDB\\Driver\\Server::executeBulkWrite()](mongodb-driver-server.executebulkwrite.md) \- Виконати одну або кілька операцій запису на сервері
