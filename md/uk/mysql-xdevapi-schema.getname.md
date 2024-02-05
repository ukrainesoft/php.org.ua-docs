---
navigation:
  - mysql-xdevapi-schema.getcollections.md: '« Schema::getCollections'
  - mysql-xdevapi-schema.getsession.md: 'Schema::getSession »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getName

(No version information available, might only be in Git)

Schema::getName — Отримує ім'я схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getName(): string
```

Отримує ім'я схеми.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я схеми у вигляді рядка, підключеного до об'єкта схеми.

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\Schema::getName()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");

// ...

var_dump($schema->getName());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(11) "addressbook"
```
