---
navigation:
  - mysql-xdevapi-collection.addorreplaceone.md: '« Collection::addOrReplaceOne'
  - mysql-xdevapi-collection.count.md: 'Collection::count »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::\_\_construct

(No version information available, might only be in Git)

Collection::\_\_construct - Конструктор класу Collection

### Опис

private **mysql\_xdevapi\\Collection::\_\_construct**()

Створює об'єкт Collection.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::getOne()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection->add('{"name": "Alfred", "age": 42, "job": "Butler"}')->execute();

// Уникальный _id (по умолчанию и рекомендуется) генерируется MySQL Server
// Возвращает сгенерированные _id; в этом Прикладе добавлена только одна запись, поэтому $ids[0]
$ids        = $result->getGeneratedIds();
$alfreds_id = $ids[0];

// ...

print_r($alfreds_id);
print_r($collection->getOne($alfreds_id));
?>
```

Висновок наведеного прикладу буде схожим на:

```
00005b6b536100000000000000b1

Array
(
    [_id] => 00005b6b536100000000000000b1
    [age] => 42
    [job] => Butler
    [name] => Alfred
)
```
