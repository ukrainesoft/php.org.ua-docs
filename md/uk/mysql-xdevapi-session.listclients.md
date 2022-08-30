Отримує список клієнтів

-   [« Session::getServerVersion](mysql-xdevapi-session.getserverversion.html)
    
-   [Session::quoteName »](mysql-xdevapi-session.quotename.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Отримує список клієнтів
    

# Session::listClients

(No version information available, might only be in Git)

Session::listClients — Отримує список клієнтів

### Опис

```methodsynopsis
public mysql_xdevapi\Session::listClients(): array
```

Отримати список клієнтських підключень до сесії сервера MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив, що містить поточні зареєстровані клієнти. Елементи масиву: "clientid", "user", "host", та "sqlsession".

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::listClients()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$ids = $session->listClients();

var_dump($ids);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  array(4) {
    ["client_id"]=>
    int(61)
    ["user"]=>
    string(4) "root"
    ["host"]=>
    string(9) "localhost"
    ["sql_session"]=>
    int(72)
  }
}
```