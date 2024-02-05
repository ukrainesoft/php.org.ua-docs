---
navigation:
  - class.mysql-xdevapi-session.md: « mysql\_xdevapi\\Session
  - mysql-xdevapi-session.commit.md: 'Session::commit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::close

(No version information available, might only be in Git)

Session::close - Закриває сесію

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

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::close()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$session->close();
```
