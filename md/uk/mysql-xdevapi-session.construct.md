---
navigation:
  - mysql-xdevapi-session.commit.html: '« Session::commit'
  - mysql-xdevapi-session.createschema.html: 'Session::createSchema »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-session.html: mysqlxdevapiSession
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
