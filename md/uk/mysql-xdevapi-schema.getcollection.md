---
navigation:
  - mysql-xdevapi-schema.existsindatabase.md: '« Schema::existsInDatabase'
  - mysql-xdevapi-schema.getcollectionastable.md: 'Schema::getCollectionAsTable »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getCollection'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getCollection

(No version information available, might only be in Git)

Schema::getCollection — Отримує колекцію зі схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getCollection(string $name): mysql_xdevapi\Collection
```

Отримує колекцію зі схеми.

### Список параметрів

`name`

Ім'я колекції для отримання.

### Значення, що повертаються

Повертає об'єкт класу Collection для вибраної колекції.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::getCollection()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();

$schema = $session->getSchema("food");
$schema->createCollection("trees");

// ...

$trees = $schema->getCollection("trees");

var_dump($trees);
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Collection)#3 (1) {
  ["name"]=>
  string(5) "trees"
}
```
