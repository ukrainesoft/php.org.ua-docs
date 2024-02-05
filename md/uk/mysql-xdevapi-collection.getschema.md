---
navigation:
  - mysql-xdevapi-collection.getone.md: '« Collection::getOne'
  - mysql-xdevapi-collection.getsession.md: 'Collection::getSession »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::getSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::getSchema

(No version information available, might only be in Git)

Collection::getSchema — Повертає об'єкт Schema

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::getSchema(): Schema Object
```

Повертає об'єкт Schema, що містить колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Schema у разі успішного виконання або **`null`**, якщо об'єкт не може бути повернутий для цієї колекції.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::getSchema()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

var_dump($collection->getSchema());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Schema)#9 (1) {
  ["name"]=>
  string(11) "addressbook"
}
```
