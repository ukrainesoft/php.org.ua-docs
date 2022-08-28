Виконує SQL запит

-   [« Session::setSavepoint](mysql-xdevapi-session.setsavepoint.html)
    
-   [Session::startTransaction »](mysql-xdevapi-session.starttransaction.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Session](class.mysql-xdevapi-session.html)
    
-   Виконує SQL запит
    

# Session::sql

(No version information available, might only be in Git)

Session::sql — Виконує запит SQL.

### Опис

```methodsynopsis
public mysql_xdevapi\Session::sql(string $query): mysql_xdevapi\SqlStatement
```

Створює власний оператор SQL. Заповнювачі підтримуються нативним синтаксисом "?". Використовує метод `execute` до виконання затвердження SQL.

### Список параметрів

`query`

Твердження SQL для виконання.

### Значення, що повертаються

Об'єкт SqlStatement.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::sql()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("CREATE DATABASE addressbook")->execute();
?>
```