---
navigation:
  - mysql-xdevapi-rowresult.construct.md: '« RowResult::\_\_construct'
  - mysql-xdevapi-rowresult.fetchone.md: 'RowResult::fetchOne »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult
title: 'RowResult::fetchAll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RowResult::fetchAll

(No version information available, might only be in Git)

RowResult::fetchAll — Отримує всі рядки з результату

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::fetchAll(): array
```

Витягує всі рядки з набору результатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий масив з усіма результатами запиту; кожен результат є асоціативний масив. Повертається порожній масив, якщо рядків немає.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\RowResult::fetchAll()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->execute()->fetchAll();

print_r($row);
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
