---
navigation:
  - mysql-xdevapi-schema.getcollection.html: '« Schema::getCollection'
  - mysql-xdevapi-schema.getcollections.html: 'Schema::getCollections »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-schema.html: mysqlxdevapiSchema
title: 'Schema::getCollectionAsTable'
---
# Schema::getCollectionAsTable

(No version information available, might only be in Git)

Schema::getCollectionAsTable — Отримати об'єкт таблиці колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getCollectionAsTable(string $name): mysql_xdevapi\Table
```

Отримати колекцію, але як об'єкт Table замість об'єкта Collection.

### Список параметрів

`name`

Ім'я колекції, з якої створюється екземпляр об'єкта Table.

### Значення, що повертаються

Об'єкт таблиці для колекції.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getCollectionAsTable()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");
$collect = $schema->createCollection("people");
$collect->add('{"name": "Fred",  "age": 21, "job": "Construction"}')->execute();
$collect->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

$table      = $schema->getCollectionAsTable("people");
$collection = $schema->getCollection("people");

var_dump($table);
var_dump($collection);
```

Результатом виконання цього прикладу буде щось подібне:

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
