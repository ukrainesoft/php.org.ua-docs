---
navigation:
  - mongodb-driver-bulkwrite.insert.html: '« MongoDBDriverBulkWrite::insert'
  - class.mongodb-driver-session.html: MongoDBDriverSession »
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.html: MongoDBDriverBulkWrite
title: 'MongoDBDriverBulkWrite::update'
---
# MongoDBDriverBulkWrite::update

(mongodb >=1.0.0)

MongoDBDriverBulkWrite::update — Додати операцію оновлення до порції

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::update(array|object $filter, array|object $newObj, ?array $updateOptions = null): void
```

Додає операцію поновлення в [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html)

### Список параметрів

`filter` (array | об'єкт)

[» Предикат запроса](https://www.mongodb.com/docs/manual/tutorial/query-documents/). Порожній предикат збігатиметься з усіма елементами колекції.

> **Зауваження**: При обчисленні критеріїв запиту, MongoDB порівнює типи та значення відповідно до власних [» правилами порівняння типів BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/), відмінних від правил [сравнения](types.comparisons.md) і [приведения типов](language.types.type-juggling.html) PHP. Коли використовується спеціальний тип BSON, критерій запиту має відповідати [классу BSON](book.bson.md) (тобто використовувати [MongoDBBSONObjectId](class.mongodb-bson-objectid.html) для вибірки по [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)

`newObj` (array | об'єкт)

Документ, що містить оператори оновлення (наприклад, `$set`), що замінює документ (наприклад, *тільки* вирази `field:value`) або [» конвейер агрегации](https://www.mongodb.com/docs/manual/reference/command/update/#update-with-an-aggregation-pipeline)

`updateOptions`

**updateOptions**

| Опция | Тип | Описание | Значение по умолчанию |
| --- | --- | --- | --- |
| arrayFilters | array |  |  |
| Масив документів фільтрів, який визначає, які елементи масиву будуть змінені для операції поновлення в полі масиву. Дивіться [» Вказуйте array Filters для операцій оновлення Масиву](https://www.mongodb.com/docs/manual/reference/command/update/#update-command-arrayfilters) у посібнику MongoDB для отримання додаткової інформації. |  |  |  |

Опція доступна з MongoDB 3.6+ і призведе до виключення під час виконання, якщо вона вказана для старої версії сервера.

| | collation | array | об'єкт |

[» Сопоставление](https://www.mongodb.com/docs/upcoming/reference/collation/) дозволяє користувачам вказувати специфічні для конкретної мови правила для порівняння рядків, такі як реакцію на регістр літер та надрядкові знаки. Якщо поставлено зіставлення, то поле `"locale"` також обов'язково. Опис полів дивіться у розділі [» Сопоставление](https://www.mongodb.com/docs/upcoming/reference/collation/#collation-document)

Якщо порівняння не задано явно, але в колекції визначено зіставлення за умовчанням, буде використано воно. Якщо немає ні того, то MongoDB буде використовувати просте бінарне порівняння рядків.

Ця опція доступна у MongoDB 3.4+ і, якщо буде використана для більш старих версій, викличе виняток під час виконання.

| | hint | string | array | об'єкт |

Індекс специфікації. Вкажіть або назву індексу у вигляді рядка, або шаблон ключа індексу. Якщо зазначено, система запитів розглядатиме плани лише з використанням індексу підказок.

Опція доступна з MongoDB 4.4+ і призведе до виключення під час виконання, якщо вона вказана для старої версії сервера.

| | multi | bool | Оновити лише перший знайдений документ, якщо **`false`** або всі відповідні документи при **`true`**. Ця опція не може бути **`true`**, коли `newObj` - Замінний документ. | **`false`** | | upsert | bool | Якщо `filter` не відповідає існуючому документу, буде вставлено *новий* документ. Документ буде створено з `newObj`якщо він замінює документ (тобто відсутні оператори оновлення); в іншому випадку оператори в `newObj` будуть застосовуватися до `filter` створення нового документа. | **`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.7.0 | Додана опція `"hint"` |
| PECL mongodb 1.6.0 | Параметр `newObj` тепер приймає конвеєр агрегації. Потрібно MongoDB 4.2+, для старішої версії сервера викине виняток під час виконання. |
| PECL mongodb 1.5.0 | Використання опції `"arrayFilters"` призведе до виключення під час виконання, якщо вона не підтримується сервером. Раніше не викидався виняток, і цей параметр, можливо, проігнорували. |
| PECL mongodb 1.4.0 | Додана опція `"arrayFilters"` |
| PECL mongodb 1.2.0 | Додана опція `"collation"` |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverBulkWrite::update()****

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->update(
    ['x' => 2],
    ['$set' => ['y' => 3]],
    ['multi' => false, 'upsert' => false]
);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

### Дивіться також

-   [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html) - Виконує одну або кілька операцій запису
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html)
