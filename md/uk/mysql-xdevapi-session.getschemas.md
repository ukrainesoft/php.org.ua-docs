- [« Session::getSchema](mysql-xdevapi-session.getschema.md)
- [Session::getServerVersion »](mysql-xdevapi-session.getserverversion.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Session](class.mysql-xdevapi-session.md)
- Отримує схеми

# Session::getSchemas

(No version information available, might only be in Git)

Session::getSchemas — Отримує схеми

### Опис

public **mysql_xdevapi\Session::getSchemas**(): array

Отримати об'єкти схеми для всіх схем, доступних у сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив, що містить об'єкти, які представляють всі схеми, доступні в
сесії.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Session::getSchemas()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schemas = $session->getSchemas();print_r($schemas); `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => mysql_xdevapi\Schema Object
(
[name] => addressbook
)
[1] => mysql_xdevapi\Schema Object
(
[name] => information_schema
)
...
