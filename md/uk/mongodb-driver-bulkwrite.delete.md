---
navigation:
  - mongodb-driver-bulkwrite.count.md: '« MongoDB\\Driver\\BulkWrite::count'
  - mongodb-driver-bulkwrite.insert.md: 'MongoDB\\Driver\\BulkWrite::insert »'
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.md: MongoDB\\Driver\\BulkWrite
title: 'MongoDB\\Driver\\BulkWrite::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\BulkWrite::delete

(mongodb >=1.0.0)

MongoDB\\Driver\\BulkWrite::delete — Додавання операції видалення порції

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::delete(array|object $filter, ?array $deleteOptions = null): void
```

Додає операцію видалення в об'єкт [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

`filter`(array|object)

[» Предикат запиту](https://www.mongodb.com/docs/manual/tutorial/query-documents/). Порожній предикат збігатиметься з усіма елементами колекції.

> **Зауваження**: При обчисленні критеріїв запиту MongoDB порівнює типи та значення відповідно до власних [» правилами порівняння типів BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/), відмінних від правил [порівняння](types.comparisons.md) і [приведення типів](language.types.type-juggling.md) PHP. Коли вказано спеціальний тип BSON, критерій запиту має відповідати [класу BSON](book.bson.md) (тобто використовувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) для вибірки по [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)

`deleteOptions`

**deleteOptions**

| Опция | Тип | Опис | Значение по умолчанию |
| --- | --- | --- | --- |
| collation | array | object |  |
| [» Зіставлення](https://www.mongodb.com/docs/upcoming/reference/collation/) дозволяє користувачам вказувати специфічні для конкретної мови правила для порівняння рядків, такі як реакцію на регістр літер та надрядкові знаки. Якщо поставлено зіставлення, то поле `"locale"`также обязательно. Опис полей смотрите в разделе[» Зіставлення](https://www.mongodb.com/docs/upcoming/reference/collation/#collation-document) |  |  |  |

Якщо зіставлення не задано явно, але в колекції визначено зіставлення за умовчанням, буде використано воно. Якщо немає ні того, то MongoDB буде використовувати просте бінарне порівняння рядків.

Ця опція доступна у MongoDB 3.4+ і, якщо буде використана для більш старих версій, викличе виняток під час виконання.

| | hint | string|array|object |

Індекс специфікації. Вкажіть або назву індексу у вигляді рядка, або шаблон ключа індексу. Якщо зазначено, система запитів розглядатиме плани лише з використанням індексу підказок.

Опція доступна з MongoDB 4.4+ і призведе до виключення під час виконання, якщо вона вказана для старої версії сервера.

| | limit | bool | Удалить все подходящие документа (**`false`**) або тільки перший знайдений документ (**`true`** **`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.8.0 | Добавлена опция`"hint"` |
| PECL mongodb 1.2.0 | Добавлена опция`"collation"` |

### Приклади

**Приклад #1 Приклад використання** MongoDB\\Driver\\BulkWrite::delete()\*\*\*\*

```php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->delete(['x' => 1], ['limit' => 1]);
$bulk->delete(['x' => 2], ['limit' => 0]);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

### Дивіться також

-   [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) \- Виконує одну або кілька операцій запису
-   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.md)
