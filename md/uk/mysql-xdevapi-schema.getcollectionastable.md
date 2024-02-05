---
navigation:
  - mysql-xdevapi-schema.getcollection.md: '« Schema::getCollection'
  - mysql-xdevapi-schema.getcollections.md: 'Schema::getCollections »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getCollectionAsTable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getCollectionAsTable

(No version information available, might only be in Git)

Schema::getCollectionAsTable — Отримує колекцію як об'єкт класу Table

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getCollectionAsTable(string $name): mysql_xdevapi\Table
```

Отримує колекцію, але як об'єкт Table замість Collection.

### Список параметрів

`name`

Ім'я колекції, з якої створюється екземпляр об'єкта Table.

### Значення, що повертаються

Повертає об'єкт класу [mysql\_xdevapi\\Table](class.mysql-xdevapi-table.md) для колекції.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::getCollectionAsTable()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");
$collect = $schema->createCollection("people");
$collect->add('{"name": "Fred",  "age": 21, "job": "Construction"}')->execute();
$collect->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

$table      = $schema->getCollectionAsTable("people");
$collection = $schema->getCollection("people");

var_dump($table);
var_dump($collection);
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Table)#4 (1) {
  ["name"]=>
  string(6) "people"
}

object(mysql_xdevapi\Collection)#5 (1) {
  ["name"]=>
  string(6) "people"
}
```
