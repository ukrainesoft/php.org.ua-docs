---
navigation:
  - mysql-xdevapi-session.commit.md: '« Session::commit'
  - mysql-xdevapi-session.createschema.md: 'Session::createSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysqlxdevapiSession
title: 'Session::construct'
---
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
