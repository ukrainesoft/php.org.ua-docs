---
navigation:
  - mysql-xdevapi-collectionfind.lockshared.md: '« CollectionFind::lockShared'
  - mysql-xdevapi-collectionfind.sort.md: 'CollectionFind::sort »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysqlxdevapiCollectionFind
title: 'CollectionFind::offset'
---
# CollectionFind::offset

(No version information available, might only be in Git)

CollectionFind::offset — Пропускає вказану кількість елементів, що повертаються.

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::offset(int $position): mysql_xdevapi\CollectionFind
```

Пропускає (зміщує) цю кількість елементів, які інакше були б повернуті операцією пошуку. Використовуйте разом із методом limit().

При значенні, що перевищує розмір набору результатів, призводить до порожнього набору.

### Список параметрів

`position`

Кількість елементів, які необхідно пропустити для операції limit().

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для додаткової обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::offset()****

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
$create
  ->add('{"name": "Reginald", "age": 42, "job": "Butler"}')
  ->execute();

// ...

$collection = $schema->getCollection("people");

$result = $collection
  ->find()
  ->sort('age asc')
  ->offset(1)
  ->limit(1)
  ->execute();

var_dump($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
