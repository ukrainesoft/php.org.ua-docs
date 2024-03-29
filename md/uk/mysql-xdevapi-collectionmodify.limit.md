---
navigation:
  - mysql-xdevapi-collectionmodify.execute.md: '« CollectionModify::execute'
  - mysql-xdevapi-collectionmodify.patch.md: 'CollectionModify::patch »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::limit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::limit

(No version information available, might only be in Git)

Collection Modify::limit — Обмежує кількість змінених документів

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::limit(int $rows): mysql_xdevapi\CollectionModify
```

Обмежує кількість документів, які змінюються цією операцією. За бажання можна використовувати skip() визначення значення зміщення.

### Список параметрів

`rows`

Максимальна кількість документів для зміни.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::limit()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$collection->add('{"name": "Fred",  "age": 21, "job": "Construction"}')->execute();
$collection->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();
$collection->add('{"name": "Betty", "age": 24, "job": "Teacher"}')->execute();

$collection
  ->modify("job = :job")
  ->bind(['job' => 'Teacher'])
  ->set('job', 'Principal')
  ->limit(1)
  ->execute();

$result = $collection
  ->find()
  ->execute();

print_r($result->fetchAll());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Array
        (
            [_id] => 00005b6b53610000000000000118
            [age] => 21
            [job] => Construction
            [name] => Fred
        )
    [1] => Array
        (
            [_id] => 00005b6b53610000000000000119
            [age] => 23
            [job] => Principal
            [name] => Wilma
        )
    [2] => Array
        (
            [_id] => 00005b6b5361000000000000011a
            [age] => 24
            [job] => Teacher
            [name] => Betty
        )
)
```
