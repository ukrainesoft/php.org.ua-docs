---
navigation:
  - mysql-xdevapi-session.getschema.md: '« Session::getSchema'
  - mysql-xdevapi-session.getserverversion.md: 'Session::getServerVersion »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::getSchemas'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::getSchemas

(No version information available, might only be in Git)

Session::getSchemas — Отримує схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Session::getSchemas(): array
```

Отримати об'єкти схеми для всіх схем, доступних у сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив, що містить об'єкти, які репрезентують всі схеми, доступні в сесії.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::getSchemas()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$schemas  = $session->getSchemas();

print_r($schemas);
```

Висновок наведеного прикладу буде схожим на:

```
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
```
