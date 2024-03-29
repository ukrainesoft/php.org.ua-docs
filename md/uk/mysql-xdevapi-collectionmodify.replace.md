---
navigation:
  - mysql-xdevapi-collectionmodify.patch.md: '« CollectionModify::patch'
  - mysql-xdevapi-collectionmodify.set.md: 'CollectionModify::set »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::replace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::replace

(No version information available, might only be in Git)

CollectionModify::replace — Замінює поле документа

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::replace(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
```

Замінює (оновлює) це значення поля новим.

### Список параметрів

`collection_field`

Шлях документа до елемента оновлення.

`expression_or_literal`

Значення, яке встановлюється для зазначеного атрибута.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::replace()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection
  ->add(
  '{"name":   "Bernie",
    "traits": ["Friend", "Brother", "Human"]}')
  ->execute();

$collection
  ->modify("name = :name")
  ->bind(['name' => 'Bernie'])
  ->replace("name", "Bern")
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
            [_id] => 00005b6b5361000000000000011b
            [name] => Bern
            [traits] => Array
                (
                    [0] => Friend
                    [1] => Brother
                    [2] => Human
                )
        )
)
```
