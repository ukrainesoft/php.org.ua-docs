---
navigation:
  - mysql-xdevapi-rowresult.getcolumncount.md: '« RowResult::getColumnsCount'
  - mysql-xdevapi-rowresult.getcolumns.md: 'RowResult::getColumns »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult
title: 'RowResult::getColumnNames'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RowResult::getColumnNames

(No version information available, might only be in Git)

RowResult::getColumnNames — Отримує всі імена стовпців

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::getColumnNames(): array
```

Отримує імена стовпців, які є у наборі результатів.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий масив імен шпальт таблиці або порожній масив, якщо набір результатів порожній.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\RowResult::getColumnNames()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE addressbook")->execute();
$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$sql = $session->sql("SELECT * from addressbook.names")->execute();

$colnames = $sql->getColumnNames();

print_r($colnames);
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => name
    [1] => age
)
```
