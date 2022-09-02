---
navigation:
  - mysql-xdevapi-session.listclients.md: '« Session::listClients'
  - mysql-xdevapi-session.releasesavepoint.md: 'Session::releaseSavepoint »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysqlxdevapiSession
title: 'Session::quoteName'
---
# Session::quoteName

(No version information available, might only be in Git)

Session::quoteName — Додає лапки

### Опис

```methodsynopsis
public mysql_xdevapi\Session::quoteName(string $name): string
```

Функція для екранування імен та ідентифікаторів SQL. Екранує ідентифікатор, вказаний відповідно до налаштувань поточного з'єднання. Цю функцію не слід використовувати для екранування значень.

### Список параметрів

`name`

Рядок для екранування.

### Значення, що повертаються

Екранований рядок.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::quoteName()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$first = "MySQL's test";
var_dump($first);
var_dump($session->quoteName($first));

$second = 'Another `test` "like" `this`';
var_dump($second);
var_dump($session->quoteName($second));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(12) "MySQL's test"
string(14) "`MySQL's test`"

string(28) "Another `test` "like" `this`"
string(34) "`Another ``test`` "like" ``this```"
```
