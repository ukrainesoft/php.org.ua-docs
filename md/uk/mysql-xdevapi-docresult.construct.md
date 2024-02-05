---
navigation:
  - class.mysql-xdevapi-docresult.md: « mysql\_xdevapi\\DocResult
  - mysql-xdevapi-docresult.fetchall.md: 'DocResult::fetchAll »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-docresult.md: mysql\_xdevapi\\DocResult
title: 'DocResult::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DocResult::\_\_construct

(No version information available, might only be in Git)

DocResult::\_\_construct — Конструктор DocResult

### Опис

private **mysql\_xdevapi\\DocResult::\_\_construct**()

Отримати результати та попередження документа, створюється CollectionFind.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання DocResult**

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$create->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();
$create->add('{"name": "Reginald", "age": 42, "job": "Butler"}')->execute();

// ...

$collection = $schema->getCollection("people");

// Возвращает объект DocResult
$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->sort('age desc')
  ->limit(1)
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
    string(28) "00005b6b536100000000000000f3"
    ["age"]=>
    int(42)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(8) "Reginald"
  }
}
```
