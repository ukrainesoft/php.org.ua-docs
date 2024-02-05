---
navigation:
  - class.mongodb-driver-bulkwrite.md: « MongoDB\\Driver\\BulkWrite
  - mongodb-driver-bulkwrite.count.md: 'MongoDB\\Driver\\BulkWrite::count »'
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.md: MongoDB\\Driver\\BulkWrite
title: 'MongoDB\\Driver\\BulkWrite::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\BulkWrite::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\BulkWrite::\_\_construct — Створює новий об'єкт BulkWrite

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::__construct(?array $options = null)
```

Створює новий [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md), який є об'єктом, що змінюється, до якого можуть бути додані одна і кілька операцій запису. Операції запису можуть бути виконані за допомогою [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)

### Список параметрів

`options`(array)

**options**

| Опция | Тип | Опис | Значение по умолчанию |
| --- | --- | --- | --- |
| bypassDocumentValidation | bool |  |  |
| Якщо **`true`**, дозволяє виконувати операції вставки або оновлення, щоб обійти перевірку рівня документа. |  |  |  |

Цей параметр доступний у MongoDB 3.2+ та ігнорується у старіших версіях сервера, які не підтримують перевірку рівня сервера.

**`false`**| | comment |[mixed](language.types.declarations.md#language.types.declarations.mixed)

Довільний коментар, що допомагає відстежити операцію за допомогою профільника бази даних, виводу CurrentOp та журналів.

Опція доступна в MongoDB 4.4+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | let | array|object |

Карта імен та значень параметрів. Значення мають бути константами або закритими виразами, які посилаються на поля документа. До параметрів можна звертатися як до змінних у контексті агрегованого виразу (наприклад, `$$var`

Опція доступна в MongoDB 5.0+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | ordered | bool | Відсортовані операції (**`true`**) виконується послідовно на сервері MongoDB, тоді як невідсортовані операції (**`false`**) відправляються на сервері у довільному порядку і можуть виконуватися паралельно. | **`true`**

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.14.0 | Додані опції `"comment"`и`"let"` |
| PECL mongodb 1.1.0 | Добавлена опция`"bypassDocumentValidation"` |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\BulkWrite::\_\_construct()\*\*\*\*

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->delete([]);
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(
    ['x' => 2],
    ['$set' => ['x' => 1]],
    ['limit' => 1, 'upsert' => false]
);
$bulk->delete(['x' => 1], ['limit' => 1]);
$bulk->update(
    ['_id' => 3],
    ['$set' => ['x' => 3]],
    ['limit' => 1, 'upsert' => true]
);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(1);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    $result = $e->getWriteResult();

    // Проверяем обеспечение гарантии записи
    if ($writeConcernError = $result->getWriteConcernError()) {
        printf("%s (%d): %s\n",
            $writeConcernError->getMessage(),
            $writeConcernError->getCode(),
            var_export($writeConcernError->getInfo(), true)
        );
    }

    // Проверяем, если какие-либо операции записи не были выполнены
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
printf("Обновлено  %d документ(ов)\n", $result->getModifiedCount());
printf("Слито %d документ(ов)\n", $result->getUpsertedCount());
printf("Удалено  %d документ(ов)\n", $result->getDeletedCount());

?>
```

Результат виконання наведеного прикладу:

```
Добавлено 2 документ(ов)
Обновлено 1 документ(ов)
Слито 1 документ(ов)
Удалено  1 документ(ов)
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) \- Виконує одну або кілька операцій запису
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
