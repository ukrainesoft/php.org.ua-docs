Опис конструктора

-   [« Session::commit](mysql-xdevapi-session.commit.html)
    
-   [Session::createSchema »](mysql-xdevapi-session.createschema.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Session](class.mysql-xdevapi-session.html)
    
-   Опис конструктора
    

# Session::construct

(No version information available, might only be in Git)

Session::construct — Опис конструктора

### Опис

private **mysqlxdevapiSession::construct**

Об'єкт Session, ініційований getSession().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->close();
?>
```