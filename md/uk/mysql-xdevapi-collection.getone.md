---
navigation:
  - mysql-xdevapi-collection.getname.md: '« Collection::getName'
  - mysql-xdevapi-collection.getschema.md: 'Collection::getSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::getOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::getOne

(No version information available, might only be in Git)

Collection::getOne — Отримує один документ

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::getOne(string $id): Document
```

Вибирає один документ із колекції.

Це короткий запис для: `Collection.find("_id = :id").bind("id", id).execute().fetchOne();`

### Список параметрів

`id`

\_id документа в колекції.

### Значення, що повертаються

Об'єкт колекції або **`null`**, якщо \_id відповідає документу.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Collection::getOne()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection->add('{"name": "Alfred", "age": 42, "job": "Butler"}')->execute();

// Уникальный _id (по умолчанию и рекомендуется) генерируется MySQL Server
// Возвращает сгенерированные _id; в этом примере только одна запись, поэтому $ids[0]
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
