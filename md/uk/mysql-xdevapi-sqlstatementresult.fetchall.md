---
navigation:
  - mysql-xdevapi-sqlstatementresult.construct.md: '« SqlStatementResult::\_\_construct'
  - mysql-xdevapi-sqlstatementresult.fetchone.md: 'SqlStatementResult::fetchOne »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-sqlstatementresult.md: mysql\_xdevapi\\SqlStatementResult
title: 'SqlStatementResult::fetchAll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий масив з усіма результатами запиту; кожен результат є асоціативний масив. Повертається порожній масив, якщо рядків немає.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\SqlStatementResult::fetchAll()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS dbtest")->execute();
$session->sql("CREATE DATABASE dbtest")->execute();
$session->sql("CREATE TABLE dbtest.workers(name text, age int, job text)")->execute();
$session->sql("INSERT INTO dbtest.workers values ('John', 42, 'bricklayer'), ('Sam', 33, 'carpenter')")->execute();

$schema = $session->getSchema("dbtest");
$table  = $schema->getTable("workers");

$rows = $session->sql("SELECT * FROM dbtest.workers")->execute()->fetchAll();

print_r($rows);
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
