Фіксує транзакцію

-   [« Session::close](mysql-xdevapi-session.close.html)
    
-   [Session::\_\_construct »](mysql-xdevapi-session.construct.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Session](class.mysql-xdevapi-session.html)
    
-   Фіксує транзакцію
    

# Session::commit

(PHP 4> = 4.4.0, PHP 5, PHP 7, PHP 8)

Session::commit - Фіксує транзакцію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::commit(): Object
```

Фіксує транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::commit()****

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("friends");

$session->startTransaction();

$collection->add('{"John":42, "Sam":33}')->execute();
$savepoint = $session->setSavepoint();

$session->commit();
$session->close();
```