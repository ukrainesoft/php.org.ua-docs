- [« Session::getServerVersion](mysql-xdevapi-session.getserverversion.md)
- [Session::quoteName »](mysql-xdevapi-session.quotename.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Session](class.mysql-xdevapi-session.md)
- Отримує список клієнтів

# Session::listClients

(No version information available, might only be in Git)

Session::listClients — Отримує список клієнтів

### Опис

public **mysql_xdevapi\Session::listClients**(): array

Отримати список клієнтських підключень до сесії сервера MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив, що містить поточні зареєстровані клієнти. Елементи
масиву: "client_id", "user", "host", та "sql_session".

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Session::listClients()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$ids = $session->listClients();var_dump($ids);?> `

Результатом виконання цього прикладу буде щось подібне:

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
