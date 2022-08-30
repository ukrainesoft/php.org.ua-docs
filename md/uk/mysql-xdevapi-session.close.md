Закриває сесію

-   [« mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   [Session::commit »](mysql-xdevapi-session.commit.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Закриває сесію
    

# Session::close

(No version information available, might only be in Git)

Session::close — Закриває сесію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::close(): bool
```

Закриває сесію із сервером.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо сесія закрита.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::close()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$session->close();
```