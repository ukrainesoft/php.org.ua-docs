---
navigation:
  - class.mysql-xdevapi-schemaobject.md: « mysql\_xdevapi\\SchemaObject
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session »
  - index.md: PHP Manual
  - class.mysql-xdevapi-schemaobject.md: mysql\_xdevapi\\SchemaObject
title: 'SchemaObject::getSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SchemaObject::getSchema

(No version information available, might only be in Git)

SchemaObject::getSchema — Отримує об'єкт схеми

### Опис

```methodsynopsis
abstract mysql_xdevapi\SchemaObject::getSchema(): mysql_xdevapi\Schema
```

Використовується іншими об'єктами для отримання схеми об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний об'єкт Schema.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::getSchema()\*\*\*\*

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
