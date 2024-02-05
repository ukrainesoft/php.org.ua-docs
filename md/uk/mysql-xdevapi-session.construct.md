---
navigation:
  - mysql-xdevapi-session.commit.md: '« Session::commit'
  - mysql-xdevapi-session.createschema.md: 'Session::createSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::\_\_construct

(No version information available, might only be in Git)

Session::\_\_construct — Опис конструктора

### Опис

private **mysql\_xdevapi\\Session::\_\_construct**()

Об'єкт Session, ініційований getSession().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->close();
?>
```
