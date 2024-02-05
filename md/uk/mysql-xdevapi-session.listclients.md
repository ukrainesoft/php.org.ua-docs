---
navigation:
  - mysql-xdevapi-session.getserverversion.md: '« Session::getServerVersion'
  - mysql-xdevapi-session.quotename.md: 'Session::quoteName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::listClients'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Масив, що містить поточні зареєстровані клієнти. Елементи масиву: "client\_id", "user", "host", та "sql\_session".

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::listClients()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$ids = $session->listClients();

var_dump($ids);
?>
```

Висновок наведеного прикладу буде схожим на:

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
