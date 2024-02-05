---
navigation:
  - mysql-xdevapi-collectionmodify.bind.md: '« CollectionModify::bind'
  - mysql-xdevapi-collectionmodify.execute.md: 'CollectionModify::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::\_\_construct

(No version information available, might only be in Git)

CollectionModify::\_\_construct - Конструктор класу CollectionModify

### Опис

private**mysql\_xdevapi\\CollectionModify::\_\_construct**()

Змінює (оновлює) колекцію та створюється методом **mysql\_xdevapi\\Collection::modify()**

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\CollectionModify::\_\_construct()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

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
