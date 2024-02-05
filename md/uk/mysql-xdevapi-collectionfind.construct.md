---
navigation:
  - mysql-xdevapi-collectionfind.bind.md: '« CollectionFind::bind'
  - mysql-xdevapi-collectionfind.execute.md: 'CollectionFind::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::\_\_construct

(No version information available, might only be in Git)

CollectionFind::\_\_construct - Конструктор класу CollectionFind

### Опис

private **mysql\_xdevapi\\CollectionFind::\_\_construct**()

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання CollectionFind**

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");
$result = $create
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
