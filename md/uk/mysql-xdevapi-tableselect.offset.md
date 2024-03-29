---
navigation:
  - mysql-xdevapi-tableselect.lockshared.md: '« TableSelect::lockShared'
  - mysql-xdevapi-tableselect.orderby.md: 'TableSelect::orderby »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::offset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::offset

(No version information available, might only be in Git)

TableSelect::offset — Встановлює межу зміщення

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::offset(int $position): mysql_xdevapi\TableSelect
```

Пропускає вказану кількість рядків у результаті.

### Список параметрів

`position`

Межа усунення.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableSelect::offset()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 42)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name', 'age')
  ->limit(1)
  ->offset(1)
  ->execute();

$row = $result->fetchAll();
print_r($row);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Array
        (
            [name] => Sam
            [age] => 42
        )
)
```
