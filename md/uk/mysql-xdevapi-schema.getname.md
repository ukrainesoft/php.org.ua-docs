---
navigation:
  - mysql-xdevapi-schema.getcollections.html: '« Schema::getCollections'
  - mysql-xdevapi-schema.getsession.html: 'Schema::getSession »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-schema.html: mysqlxdevapiSchema
title: 'Schema::getName'
---
# Schema::getName

(No version information available, might only be in Git)

Schema::getName — Отримати ім'я схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getName(): string
```

Отримати назву схеми.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я схеми у вигляді рядка, підключеного до об'єкта схеми.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getName()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");

// ...

var_dump($schema->getName());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "addressbook"
```
