---
navigation:
  - mongodb-driver-bulkwrite.count.md: '« MongoDBDriverBulkWrite::count'
  - mongodb-driver-bulkwrite.insert.md: 'MongoDBDriverBulkWrite::insert »'
  - index.md: PHP Manual
  - class.mongodb-driver-bulkwrite.md: MongoDBDriverBulkWrite
title: 'MongoDBDriverBulkWrite::delete'
---
# MongoDBDriverBulkWrite::delete

(mongodb >=1.0.0)

MongoDBDriverBulkWrite::delete — Додавання операції видалення порції

### Опис

```methodsynopsis
public MongoDB\Driver\BulkWrite::delete(array|object $filter, ?array $deleteOptions = null): void
```

Додає операцію видалення в об'єкт [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.md)

### Список параметрів

`filter` (array | об'єкт)

[» Предикат запроса](https://www.mongodb.com/docs/manual/tutorial/query-documents/). Порожній предикат збігатиметься з усіма елементами колекції.

> **Зауваження**: При обчисленні критеріїв запиту, MongoDB порівнює типи та значення відповідно до власних [» правилами порівняння типів BSON](https://www.mongodb.com/docs/manual/reference/bson-type-comparison-order/), відмінних від правил [сравнения](types.comparisons.md) і [приведения типов](language.types.type-juggling.md) PHP. Коли використовується спеціальний тип BSON, критерій запиту має відповідати [классу BSON](book.bson.md) (тобто використовувати [MongoDBBSONObjectId](class.mongodb-bson-objectid.md) для вибірки по [» ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)

`deleteOptions`

**deleteOptions**

| Опция | Тип | Описание | Значение по умолчанию |
| --- | --- | --- | --- |
| collation | array | object |  |
| [» Сопоставление](https://www.mongodb.com/docs/upcoming/reference/collation/) дозволяє користувачам вказувати специфічні для конкретної мови правила для порівняння рядків, такі як реакцію на регістр літер та надрядкові знаки. Якщо поставлено зіставлення, то поле `"locale"` також обов'язково. Опис полів дивіться у розділі [» Сопоставление](https://www.mongodb.com/docs/upcoming/reference/collation/#collation-document) |  |  |  |

Якщо порівняння не задано явно, але в колекції визначено зіставлення за умовчанням, буде використано воно. Якщо немає ні того, то MongoDB буде використовувати просте бінарне порівняння рядків.

Ця опція доступна у MongoDB 3.4+ і, якщо буде використана для більш старих версій, викличе виняток під час виконання.

| | hint | string | array | об'єкт |

Індекс специфікації. Вкажіть або назву індексу у вигляді рядка, або шаблон ключа індексу. Якщо зазначено, система запитів розглядатиме плани лише з використанням індексу підказок.

Опція доступна з MongoDB 4.4+ і призведе до виключення під час виконання, якщо вона вказана для старої версії сервера.

| | limit | bool | Видалити всі відповідні документи (**`false`**) або тільки перший знайдений документ (**`true`** **`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.8.0 | Додана опція `"hint"` |
| PECL mongodb 1.2.0 | Додана опція `"collation"` |

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverBulkWrite::delete()****

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

-   [MongoDBDriverManager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md) - Виконує одну або кілька операцій запису
-   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.md)
