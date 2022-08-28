Отримує кількість стовпців

-   [« RowResult::fetchOne](mysql-xdevapi-rowresult.fetchone.html)
    
-   [RowResult::getColumnNames »](mysql-xdevapi-rowresult.getcolumnnames.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\RowResult](class.mysql-xdevapi-rowresult.html)
    
-   Отримує кількість стовпців
    

# RowResult::getColumnsCount

(No version information available, might only be in Git)

RowResult::getColumnsCount — Отримує кількість стовпців

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::getColumnsCount(): int
```

Отримує кількість стовпців, які є у наборі результатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість стовпців; 0 якщо їх немає

### список змін

| Версия | Описание |
| --- | --- |
|  | Метод перейменований з getColumnCount() на getColumnsCount(). |

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiRowResult::getColumnsCount()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE addressbook")->execute();
$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$sql = $session->sql("SELECT * from addressbook.names")->execute();

echo $sql->getColumnsCount();
```

Результатом виконання цього прикладу буде щось подібне:

```
2
```