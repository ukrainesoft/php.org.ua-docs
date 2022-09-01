---
navigation:
  - mysql-xdevapi-sqlstatementresult.construct.html: '« SqlStatementResult::construct'
  - mysql-xdevapi-sqlstatementresult.fetchone.html: 'SqlStatementResult::fetchOne »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-sqlstatementresult.html: mysqlxdevapiSqlStatementResult
title: 'SqlStatementResult::fetchAll'
---
# SqlStatementResult::fetchAll

(No version information available, might only be in Git)

SqlStatementResult::fetchAll — Отримує всі рядки з результату

### Опис

```methodsynopsis
public mysql_xdevapi\SqlStatementResult::fetchAll(): array
```

Витягує всі рядки з набору результатів.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий масив із усіма результатами запиту; кожен результат є асоціативний масив. Повертається порожній масив, якщо рядків немає.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSqlStatementResult::fetchAll()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS dbtest")->execute();
$session->sql("CREATE DATABASE dbtest")->execute();
$session->sql("CREATE TABLE dbtest.workers(name text, age int, job text)")->execute();
$session->sql("INSERT INTO dbtest.workers values ('John', 42, 'bricklayer'), ('Sam', 33, 'carpenter')")->execute();

$schema = $session->getSchema("dbtest");
$table  = $schema->getTable("workers");

$rows = $session->sql("SELECT * FROM dbtest.workers")->execute()->fetchAll();

print_r($rows);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
