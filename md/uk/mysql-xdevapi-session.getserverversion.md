Отримує версію сервера

-   [« Session::getSchemas](mysql-xdevapi-session.getschemas.html)
    
-   [Session::listClients »](mysql-xdevapi-session.listclients.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Отримує версію сервера
    

# Session::getServerVersion

(No version information available, might only be in Git)

Session::getServerVersion — Отримує версію сервера

### Опис

```methodsynopsis
public mysql_xdevapi\Session::getServerVersion(): int
```

Отримує версію MySQL для сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Версія сервера MySQL для сесії у вигляді цілого числа, такого як "80012".

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::getServerVersion()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$version = $session->getServerVersion();

var_dump($version);
```

Результатом виконання цього прикладу буде щось подібне:

```
int(80012)
```