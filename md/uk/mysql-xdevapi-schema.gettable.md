---
navigation:
  - mysql-xdevapi-schema.getsession.md: '« Schema::getSession'
  - mysql-xdevapi-schema.gettables.md: 'Schema::getTables »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getTable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getTable

(No version information available, might only be in Git)

Schema::getTable — Отримує таблицю схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getTable(string $name): mysql_xdevapi\Table
```

Отримує об'єкт класу Table для зазначеної таблиці у схемі.

### Список параметрів

`name`

Ім'я таблиці.

### Значення, що повертаються

Повертає об'єкт класу Table.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::getTable()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->execute()->fetchAll();

print_r($row);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Array
        (
            [name] => John
            [age] => 42
        )
    [1] => Array
        (
            [name] => Sam
            [age] => 33
        )
)
```
