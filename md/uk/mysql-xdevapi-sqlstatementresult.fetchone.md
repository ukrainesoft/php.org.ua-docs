---
navigation:
  - mysql-xdevapi-sqlstatementresult.fetchall.html: '« SqlStatementResult::fetchAll'
  - mysql-xdevapi-sqlstatementresult.getaffecteditemscount.html: 'SqlStatementResult::getAffectedItemsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-sqlstatementresult.html: mysqlxdevapiSqlStatementResult
title: 'SqlStatementResult::fetchOne'
---
# SqlStatementResult::fetchOne

(No version information available, might only be in Git)

SqlStatementResult::fetchOne — Отримує один рядок

### Опис

```methodsynopsis
public mysql_xdevapi\SqlStatementResult::fetchOne(): array
```

Отримує один рядок із набору результатів.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Результат як асоціативний масив. У разі відсутності результату повертається нуль.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSqlStatementResult::fetchOne()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS dbtest")->execute();
$session->sql("CREATE DATABASE dbtest")->execute();
$session->sql("CREATE TABLE dbtest.workers(name text, age int, job text)")->execute();
$session->sql("INSERT INTO dbtest.workers values ('John', 42, 'bricklayer'), ('Sam', 33, 'carpenter')")->execute();

$schema = $session->getSchema("dbtest");
$table  = $schema->getTable("workers");

$rows = $session->sql("SELECT * FROM dbtest.workers")->execute()->fetchOne();

print_r($rows);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [name] => John
    [age] => 42
    [job] => bricklayer
)
```
