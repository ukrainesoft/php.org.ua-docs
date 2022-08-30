Створює точку збереження

-   [« Session::rollbackTo](mysql-xdevapi-session.rollbackto.html)
    
-   [Session::sql »](mysql-xdevapi-session.sql.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Створює точку збереження
    

# Session::setSavepoint

(No version information available, might only be in Git)

Session::setSavepoint — Створення точки збереження

### Опис

```methodsynopsis
public mysql_xdevapi\Session::setSavepoint(string $name = ?): string
```

Створює нову точку збереження транзакції.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`name`

Назва точки збереження. Ім'я генерується автоматично, якщо необов'язковий параметр `name` не визначено, як 'SAVEPOINT 1', 'SAVEPOINT 2' і т.д.

### Значення, що повертаються

Назва точки збереження.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::setSavepoint()****

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