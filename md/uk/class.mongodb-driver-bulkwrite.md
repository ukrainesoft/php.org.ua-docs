---
navigation:
  - mongodb-driver-query.construct.md: '« MongoDB\\Driver\\Query::\_\_construct'
  - mongodb-driver-bulkwrite.construct.md: 'MongoDB\\Driver\\BulkWrite::\_\_construct »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\BulkWrite
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\BulkWrite

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\BulkWrite** збирає одну або кілька операцій запису, які мають бути надіслані на сервер. Після додавання будь-якої кількості операцій вставки, оновлення або видалення колекція може бути виконана за допомогою [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)

Операції запису можуть бути відсортовані (за замовчуванням) або відсортовані. Відсортовані операції запису надсилаються на сервер у вказаному порядку для послідовного виконання. У разі виникнення помилки запису, будь-які операції, що залишилися, будуть перервані. Невідсортовані операції надсилаються на сервер у довільному порядку, де вони можуть виконуватися паралельно. Повідомлення про помилки, які виникають, будуть надіслані після виконання всіх операцій.

## Огляд класів

```classsynopsis



    
     final
     
      class MongoDB\Driver\BulkWrite
     

     implements 
       Countable {


    /* Методы */
    
   public __construct(?array $options = null)
public count(): int
public delete(array|object $filter, ?array $deleteOptions = null): void
public insert(array|object $document): mixed
public update(array|object $filter, array|object $newObj, ?array $updateOptions = null): void

   }
```

## Приклади

**Приклад #1 Змішані операції групуються за типом**

Змішані операції запису (тобто додавання, оновлення або видалення) будуть зібрані в типізовані команди запису, які будуть послідовно відправлені на сервер.

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(['x' => 2], ['$set' => ['x' => 1]]);
$bulk->insert(['_id' => 3, 'x' => 3]);
$bulk->delete(['x' => 1]);

?>
```

В результаті буде виконано чотири команди запису (тобто звернень). Оскільки операції відсортовані, третя вставка не може бути надіслана, доки не буде виконано попереднє оновлення.

**Приклад #2 Відсортовані операції запису, що викликають помилку**

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->delete([]);
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 3, 'hello' => 'world']);
$bulk->update(['_id' => 3], ['$set' => ['hello' => 'earth']]);
$bulk->insert(['_id' => 4, 'hello' => 'pluto']);
$bulk->update(['_id' => 4], ['$set' => ['hello' => 'moon']]);
$bulk->insert(['_id' => 3]);
$bulk->insert(['_id' => 4]);
$bulk->insert(['_id' => 5]);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 1000);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    $result = $e->getWriteResult();

    // Убедиться, что гарантия записи не может быть выполнена
    if ($writeConcernError = $result->getWriteConcernError()) {
        printf("%s (%d): %s\n",
            $writeConcernError->getMessage(),
            $writeConcernError->getCode(),
            var_export($writeConcernError->getInfo(), true)
        );
    }

    // Проверить, не выполнялись ли какие-либо операции записи
    foreach ($result->getWriteErrors() as $writeError) {
        printf("Operation#%d: %s (%d)\n",
            $writeError->getIndex(),
            $writeError->getMessage(),
            $writeError->getCode()
        );
    }
} catch (MongoDB\Driver\Exception\Exception $e) {
    printf("Другая ошибка: %s\n", $e->getMessage());
    exit;
}

printf("Добавлено %d документ(ов)\n", $result->getInsertedCount());
printf("Обновлено %d документ(ов)\n", $result->getModifiedCount());

?>
```

Результат виконання наведеного прикладу:

```
Operation#7: E11000 duplicate key error index: db.collection.$_id_ dup key: { : 3 } (11000)
Добавлено 4 документ(ов)
Обновлено 2 документ(ов)
```

Якщо гарантія запису не може бути виконана, результат наведеного вище прикладу буде щось на кшталт цього:

```
waiting for replication timed out (64): array (
  'wtimeout' => true,
)
Operation#7: E11000 duplicate key error index: databaseName.collectionName.$_id_ dup key: { : 3 } (11000)
Inserted 4 document(s)
Updated  2 document(s)
```

Якщо ми виконаємо приклад вище, але розв'яжемо невідсортовані записи:

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => false]);
/* ... */

?>
```

Результат виконання наведеного прикладу:

```
Operation#7: E11000 duplicate key error index: db.collection.$_id_ dup key: { : 3 } (11000)
Operation#8: E11000 duplicate key error index: db.collection.$_id_ dup key: { : 4 } (11000)
Inserted 5 document(s)
Updated  2 document(s)
```

## Дивіться також

-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
-   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)
-   [MongoDB\\Driver\\WriteConcernError](class.mongodb-driver-writeconcernerror.md)
-   [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.md)

## Зміст

-   [MongoDB\\Driver\\BulkWrite::\_\_construct](mongodb-driver-bulkwrite.construct.md)— Створює новий об'єкт BulkWrite
-   [MongoDB\\Driver\\BulkWrite::count](mongodb-driver-bulkwrite.count.md) \- Підраховує кількість операцій запису в порції
-   [MongoDB\\Driver\\BulkWrite::delete](mongodb-driver-bulkwrite.delete.md)— Додавання операції видалення порції
-   [MongoDB\\Driver\\BulkWrite::insert](mongodb-driver-bulkwrite.insert.md) \- Додати операцію вставки в порцію
-   [MongoDB\\Driver\\BulkWrite::update](mongodb-driver-bulkwrite.update.md)— Додати операцію оновлення до порції
