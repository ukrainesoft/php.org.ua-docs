---
navigation:
  - mysql-xdevapi-collectionfind.execute.md: '« CollectionFind::execute'
  - mysql-xdevapi-collectionfind.groupby.md: 'CollectionFind::groupBy »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::fields'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::fields

(No version information available, might only be in Git)

CollectionFind::fields — Встановлює фільтр поля документа

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::fields(string $projection): mysql_xdevapi\CollectionFind
```

Визначає стовпці, які мають повернути запит. Якщо не визначено, то повертаються усі стовпці.

### Список параметрів

`projection`

Може бути або одним рядком або масивом рядків, що визначають стовпці, які потрібно повернути для кожного документа, який відповідає умові пошуку.

### Значення, що повертаються

Повертає об'єкт класу CollectionFind, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionFind::fields()\*\*\*\*

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
  ->fields('name')
  ->execute();

var_dump($result->fetchAll());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [0]=>
  array(1) {
    ["name"]=>
    string(6) "Alfred"
  }
}
```
