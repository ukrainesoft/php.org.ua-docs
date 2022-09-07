---
navigation:
  - mysql-xdevapi-collectionmodify.bind.md: '« CollectionModify::bind'
  - mysql-xdevapi-collectionmodify.execute.md: 'CollectionModify::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysqlxdevapiCollectionModify
title: 'CollectionModify::construct'
---
# CollectionModify::construct

(No version information available, might only be in Git)

CollectionModify::construct - Конструктор класу CollectionModify

### Опис

private **mysqlxdevapiCollectionModify::construct**

Змінює (оновлює) колекцію та створюється методом Collection::modify().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::construct()****

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
  ->modify("name in ('Bernie', 'Jane')")
  ->arrayAppend('traits', 'Happy')
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
            [_id] => 00005b6b5361000000000000010c
            [name] => Bernie
            [traits] => Array
                (
                    [0] => Friend
                    [1] => Brother
                    [2] => Human
                    [3] => Happy
                )
        )
)
```
