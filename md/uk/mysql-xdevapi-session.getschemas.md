---
navigation:
  - mysql-xdevapi-session.getschema.html: '« Session::getSchema'
  - mysql-xdevapi-session.getserverversion.html: 'Session::getServerVersion »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.html: mysqlxdevapiSession
title: 'Session::getSchemas'
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

**Приклад #1 Приклад використання **mysqlxdevapiSession::getSchemas()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$schemas  = $session->getSchemas();

print_r($schemas);
```

Результатом виконання цього прикладу буде щось подібне:

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
