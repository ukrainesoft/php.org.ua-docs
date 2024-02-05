---
navigation:
  - mysql-xdevapi-collectionfind.construct.md: '« CollectionFind::\_\_construct'
  - mysql-xdevapi-collectionfind.fields.md: 'CollectionFind::fields »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::execute

(No version information available, might only be in Git)

CollectionFind::execute — Виконує затвердження

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::execute(): mysql_xdevapi\DocResult
```

Виконує операцію пошуку; ця функціональність дозволена для ланцюжка методів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт класу [mysql\_xdevapi\\DocResult](class.mysql-xdevapi-docresult.md), з якого можна отримати результати, або запросити стан операції.

### Приклади

**Приклад #1 Приклад використання класу CollectionFind**

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$create
  ->add('{"name": "Alfred", "age": 18, "job": "Butler"}')
  ->execute();

// ...

$collection = $schema->getCollection("people");

$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->execute();

var_dump($result->fetchAll());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [0]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b536100000000000000cf"
    ["age"]=>
    int(18)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(6) "Alfred"
  }
}
```
