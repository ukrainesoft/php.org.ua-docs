Відкочує транзакцію

-   [« Session::releaseSavepoint](mysql-xdevapi-session.releasesavepoint.html)
    
-   [Session::rollbackTo »](mysql-xdevapi-session.rollbackto.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Відкочує транзакцію
    

# Session::rollback

(No version information available, might only be in Git)

Session::rollback - Відкочує транзакцію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::rollback(): void
```

Відкочує транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::rollback()****

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("names");

$session->startTransaction();
$collection->add( '{"test1":1, "test2":2}' )->execute();

$savepoint = $session->setSavepoint();

$collection->add( '{"test3":3, "test4":4}' )->execute();

$session->releaseSavepoint($savepoint);
$session->rollback();
?>
```