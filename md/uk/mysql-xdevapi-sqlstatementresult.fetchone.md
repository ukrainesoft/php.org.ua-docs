---
navigation:
  - mysql-xdevapi-sqlstatementresult.fetchall.md: '« SqlStatementResult::fetchAll'
  - mysql-xdevapi-sqlstatementresult.getaffecteditemscount.md: 'SqlStatementResult::getAffectedItemsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-sqlstatementresult.md: mysql\_xdevapi\\SqlStatementResult
title: 'SqlStatementResult::fetchOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Результат як асоціативний масив. У разі відсутності результату повертається нуль.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\SqlStatementResult::fetchOne()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS dbtest")->execute();
$session->sql("CREATE DATABASE dbtest")->execute();
$session->sql("CREATE TABLE dbtest.workers(name text, age int, job text)")->execute();
$session->sql("INSERT INTO dbtest.workers values ('John', 42, 'bricklayer'), ('Sam', 33, 'carpenter')")->execute();

$schema = $session->getSchema("dbtest");
$table  = $schema->getTable("workers");

$rows = $session->sql("SELECT * FROM dbtest.workers")->execute()->fetchOne();

print_r($rows);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [name] => John
    [age] => 42
    [job] => bricklayer
)
```
