---
navigation:
  - class.mysql-xdevapi-session.md: « mysqlxdevapiSession
  - mysql-xdevapi-session.commit.md: 'Session::commit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysqlxdevapiSession
title: 'Session::close'
---
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
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$session->close();
```
