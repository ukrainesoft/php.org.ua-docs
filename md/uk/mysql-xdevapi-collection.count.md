---
navigation:
  - mysql-xdevapi-collection.construct.md: '« Collection::\_\_construct'
  - mysql-xdevapi-collection.createindex.md: 'Collection::createIndex »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::count

(No version information available, might only be in Git)

Collection::count — Отримує кількість документів

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::count(): int
```

Функціонал аналогічний операції SQL `SELECT COUNT(*)` на сервері MySQL для поточної схеми та колекції. Іншими словами, метод підраховує кількість документів у колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість документів у колекції.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::count()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

$result = $collection
  ->add(
  '{"name": "Bernie",
    "jobs": [
      {"title":"Cat Herder","Salary":42000},
      {"title":"Father","Salary":0}
    ],
    "hobbies": ["Sports","Making cupcakes"]}',
  '{"name": "Jane",
    "jobs": [
      {"title":"Scientist","Salary":18000},
      {"title":"Mother","Salary":0}
    ],
    "hobbies": ["Walking","Making pies"]}')
  ->execute();

var_dump($collection->count());
?>
```

Результат виконання наведеного прикладу:

```
int(2)
```
