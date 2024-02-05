---
navigation:
  - mysql-xdevapi-session.getdefaultschema.md: '« Session::getDefaultSchema'
  - mysql-xdevapi-session.getschemas.md: 'Session::getSchemas »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::getSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::getSchema

(No version information available, might only be in Git)

Session::getSchema — Отримує новий об'єкт схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Session::getSchema(string $schema_name): mysql_xdevapi\Schema
```

Новий об'єкт Schema для вказаного імені схеми.

### Список параметрів

`schema_name`

Ім'я схеми (бази даних), на яку потрібно отримати об'єкт Schema.

### Значення, що повертаються

Об'єкт Schema.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::getSchema()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$schema  = $session->getSchema("addressbook");

print_r($schema);
```

Висновок наведеного прикладу буде схожим на:

```
mysql_xdevapi\Schema Object
(
    [name] => addressbook
)
```
