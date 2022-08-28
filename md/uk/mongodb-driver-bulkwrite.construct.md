Створює новий об'єкт BulkWrite

-   [« MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html)
    
-   [MongoDB\\Driver\\BulkWrite::count »](mongodb-driver-bulkwrite.count.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html)
    
-   Створює новий об'єкт BulkWrite
    

# MongoDBDriverBulkWrite::construct

(mongodb >=1.0.0)

MongoDBDriverBulkWrite::construct — Створює новий об'єкт BulkWrite

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::__construct(?array $options = null)
```

Створює новий [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html), який є об'єктом, що змінюється, до якого можуть бути додані одна і кілька операцій запису. Операції запису можуть бути виконані за допомогою [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html)

### Список параметрів

`options` (array)

**options**

| Опция                                                                                                      | Тип  | Описание | Значение по умолчанию |
|------------------------------------------------------------------------------------------------------------|------|----------|-----------------------|
| bypassDocumentValidation                                                                                   | bool |          |                       |
| Якщо **`true`**, дозволяє виконувати операції вставки або оновлення, щоб обійти перевірку рівня документа. |      |          |                       |

Цей параметр доступний у MongoDB 3.2+ та ігнорується у старіших версіях сервера, які не підтримують перевірку рівня сервера.

**`false`** | | comment | [mixed](language.types.declarations.html#language.types.declarations.mixed)

Довільний коментар, що допомагає відстежити операцію за допомогою профільника бази даних, виводу CurrentOp та журналів.

Опція доступна в MongoDB 4.4+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | let | array | об'єкт |

Карта імен та значень параметрів. Значення мають бути константами або закритими виразами, які посилаються на поля документа. До параметрів можна звертатися як до змінних у контексті агрегованого виразу (наприклад, `$$var`

Опція доступна в MongoDB 5.0+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | ordered | bool | Відсортовані операції (**`true`**) виконується послідовно на сервері MongoDB, тоді як невідсортовані операції (**`false`**) відправляються на сервері у довільному порядку і можуть виконуватися паралельно. | **`true`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия              | Описание                                  |
|---------------------|-------------------------------------------|
| PECL mongodb 1.14.0 | Додані опції `"comment"` і `"let"`        |
| PECL mongodb 1.1.0  | Додана опція `"bypassDocumentValidation"` |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverBulkWrite::construct()****

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->delete([]);
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(
    ['x' => 2],
    ['$set' => ['x' => 1]],
    ['limit' => 1, 'upsert' => false]
);
$bulk->delete(['x' => 1], ['limit' => 1]);
$bulk->update(
    ['_id' => 3],
    ['$set' => ['x' => 3]],
    ['limit' => 1, 'upsert' => true]
);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(1);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    $result = $e->getWriteResult();

    // Проверяем обеспечение гарантии записи
    if ($writeConcernError = $result->getWriteConcernError()) {
        printf("%s (%d): %s\n",
            $writeConcernError->getMessage(),
            $writeConcernError->getCode(),
            var_export($writeConcernError->getInfo(), true)
        );
    }

    // Проверяем, если какие-либо операции записи не были выполнены
    foreach ($result->getWriteErrors() as $writeError) {
        printf("Operation#%d: %s (%d)\n",
            $writeError->getIndex(),
            $writeError->getMessage(),
            $writeError->getCode()
        );
    }
} catch (MongoDB\Driver\Exception\Exception $e) {
    printf("Другая ошибка: %s\n", $e->getMessage());
    exit;
}

printf("Добавлено %d документ(ов)\n", $result->getInsertedCount());
printf("Обновлено  %d документ(ов)\n", $result->getModifiedCount());
printf("Слито %d документ(ов)\n", $result->getUpsertedCount());
printf("Удалено  %d документ(ов)\n", $result->getDeletedCount());

?>
```

Результат виконання цього прикладу:

```
Добавлено 2 документ(ов)
Обновлено 1 документ(ов)
Слито 1 документ(ов)
Удалено  1 документ(ов)
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html) - Виконує одну або кілька операцій запису
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html)