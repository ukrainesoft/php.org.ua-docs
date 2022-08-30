Отримує всі імена стовпців

-   [« RowResult::getColumnsCount](mysql-xdevapi-rowresult.getcolumncount.html)
    
-   [RowResult::getColumns »](mysql-xdevapi-rowresult.getcolumns.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiRowResult](class.mysql-xdevapi-rowresult.html)
    
-   Отримує всі імена стовпців
    

# RowResult::getColumnNames

(No version information available, might only be in Git)

RowResult::getColumnNames — Отримує всі імена стовпців

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::getColumnNames(): array
```

Отримує імена стовпців, які є у наборі результатів.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий масив імен шпальт таблиці або порожній масив, якщо набір результатів порожній.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiRowResult::getColumnNames()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE addressbook")->execute();
$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$sql = $session->sql("SELECT * from addressbook.names")->execute();

$colnames = $sql->getColumnNames();

print_r($colnames);
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => name
    [1] => age
)
```