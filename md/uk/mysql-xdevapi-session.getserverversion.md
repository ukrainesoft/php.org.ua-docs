---
navigation:
  - mysql-xdevapi-session.getschemas.md: '« Session::getSchemas'
  - mysql-xdevapi-session.listclients.md: 'Session::listClients »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::getServerVersion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Версія MySQL для сесії у вигляді цілого числа, такого як "80012".

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::getServerVersion()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$version = $session->getServerVersion();

var_dump($version);
```

Висновок наведеного прикладу буде схожим на:

```
int(80012)
```
