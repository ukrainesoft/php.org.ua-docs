---
navigation:
  - mysql-xdevapi-collectionmodify.replace.md: '« CollectionModify::replace'
  - mysql-xdevapi-collectionmodify.skip.md: 'CollectionModify::skip »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysqlxdevapiCollectionModify
title: 'CollectionModify::set'
---
# CollectionModify::set

(No version information available, might only be in Git)

CollectionModify::set — Встановлює атрибут документа

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::set(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
```

Встановлює чи оновлює атрибути документів у колекції.

### Список параметрів

`collection_field`

Шлях до документа (назва) елемента для установки.

`expression_or_literal`

Значення для встановлення.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::set()****

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
  ->set("name", "Bern")
  ->execute();

$result = $collection
  ->find()
  ->execute();

print_r($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [_id] => 00005b6b53610000000000000111
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
