Починає транзакцію

-   [« Session::sql](mysql-xdevapi-session.sql.html)
    
-   [mysqlxdevapiSqlStatement »](class.mysql-xdevapi-sqlstatement.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Починає транзакцію
    

# Session::startTransaction

(No version information available, might only be in Git)

Session::startTransaction - Починає транзакцію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::startTransaction(): void
```

Починає нову транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::startTransaction()****

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("friends");

$session->startTransaction();
$collection->add( '{"test1":1, "test2":2}' )->execute();

$savepoint = $session->setSavepoint();

$collection->add( '{"test3":3, "test4":4}' )->execute();

$session->releaseSavepoint($savepoint);
$session->rollback();
?>
```