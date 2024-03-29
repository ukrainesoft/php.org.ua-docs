---
navigation:
  - mongodb-driver-bulkwrite.insert.md: '« MongoDB\\Driver\\BulkWrite::insert'
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session »
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.md: MongoDB\\Driver\\BulkWrite
title: 'MongoDB\\Driver\\BulkWrite::update'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\BulkWrite::update

(mongodb >=1.0.0)

MongoDB\\Driver\\BulkWrite::update — Додати операцію оновлення до порції

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::update(array|object $filter, array|object $newObj, ?array $updateOptions = null): void
```

Добавляет операцию обновления в[MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

`filter`(array|object)

[» Предикат запиту](https://www.mongodb.com/docs/manual/tutorial/query-documents/). Порожній предикат збігатиметься з усіма елементами колекції.

> **Зауваження**: При обчисленні критеріїв запиту MongoDB порівнює типи та значення відповідно до власних [» правилами порівняння типів BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/), відмінних від правил [порівняння](types.comparisons.md) і [приведення типів](language.types.type-juggling.md) PHP. Коли вказано спеціальний тип BSON, критерій запиту має відповідати [класу BSON](book.bson.md) (тобто використовувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) для вибірки по [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)

`newObj`(array|object)

Документ, що містить оператори оновлення (наприклад, `$set`), заменяющий документ (наПриклад,*тільки* вирази `field:value`) или[» конвеєр агрегації](https://www.mongodb.com/docs/manual/reference/command/update/#update-with-an-aggregation-pipeline)

`updateOptions`

**updateOptions**

| Опция | Тип | Опис | Значение по умолчанию |
| --- | --- | --- | --- |
| arrayFilters | array |  |  |
| Масив документів фільтрів, який визначає, які елементи масиву будуть змінені для операції поновлення в полі масиву. Дивіться [» Вказуйте arrayFilters для операцій оновлення масиву](https://www.mongodb.com/docs/manual/reference/command/update/#update-command-arrayfilters) у посібнику MongoDB для отримання додаткової інформації. |  |  |  |

Опція доступна з MongoDB 3.6+ і призведе до виключення під час виконання, якщо вона вказана для старої версії сервера.

| | collation | array|object |

[» Зіставлення](https://www.mongodb.com/docs/upcoming/reference/collation/) дозволяє користувачам вказувати специфічні для конкретної мови правила для порівняння рядків, такі як реакцію на регістр літер та надрядкові знаки. Якщо поставлено зіставлення, то поле `"locale"`также обязательно. Опис полей смотрите в разделе[» Зіставлення](https://www.mongodb.com/docs/upcoming/reference/collation/#collation-document)

Якщо зіставлення не задано явно, але в колекції визначено зіставлення за умовчанням, буде використано воно. Якщо немає ні того, то MongoDB буде використовувати просте бінарне порівняння рядків.

Ця опція доступна у MongoDB 3.4+ і, якщо буде використана для більш старих версій, викличе виняток під час виконання.

| | hint | string|array|object |

Індекс специфікації. Вкажіть або назву індексу у вигляді рядка, або шаблон ключа індексу. Якщо зазначено, система запитів розглядатиме плани лише з використанням індексу підказок.

Опція доступна з MongoDB 4.4+ і призведе до виключення під час виконання, якщо вона вказана для старої версії сервера.

| | multi | bool | Оновити лише перший знайдений документ, якщо **`false`** або всі відповідні документи при **`true`**. Ця опція не може бути **`true`**, когда`newObj`\- заменяющий документ. |**`false`**| | upsert | bool | Если`filter`не соответствует существующему документу, будет вставлен*новий*документ. Документ будет создан из`newObj`якщо він замінює документ (тобто відсутні оператори оновлення); в іншому випадку оператори в `newObj`будут применяться к`filter`для создания нового документа. |**`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.7.0 | Добавлена опция`"hint"` |
| PECL mongodb 1.6.0 | Параметр`newObj` тепер приймає конвеєр агрегації. Потрібно MongoDB 4.2+, для старішої версії сервера викине виняток під час виконання. |
| PECL mongodb 1.5.0 | Використання опції `"arrayFilters"` призведе до виключення під час виконання, якщо вона не підтримується сервером. Раніше не викидався виняток, і цей параметр, можливо, проігнорували. |
| PECL mongodb 1.4.0 | Добавлена опция`"arrayFilters"` |
| PECL mongodb 1.2.0 | Добавлена опция`"collation"` |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\BulkWrite::update()\*\*\*\*

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->update(
    ['x' => 2],
    ['$set' => ['y' => 3]],
    ['multi' => false, 'upsert' => false]
);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) \- Виконує одну або кілька операцій запису
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
