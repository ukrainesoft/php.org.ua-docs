---
navigation:
  - mysql-xdevapi-schema.getcollectionastable.md: '« Schema::getCollectionAsTable'
  - mysql-xdevapi-schema.getname.md: 'Schema::getName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getCollections'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getCollections

(No version information available, might only be in Git)

Schema::getCollections — Отримує всі колекції схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getCollections(): array
```

Отримує список колекцій цієї схеми.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив усіх колекцій у цій схемі, де кожне значення елемента масиву є об'єктом класу Collection з ім'ям колекції як ключ.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::getCollections()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");
$collect = $schema->createCollection("people");
$collect->add('{"name": "Fred",  "age": 21, "job": "Construction"}')->execute();
$collect->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

$collections = $schema->getCollections();
var_dump($collections);
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  ["people"]=>
  object(mysql_xdevapi\Collection)#4 (1) {
    ["name"]=>
    string(6) "people"
  }
}
```
