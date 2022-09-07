---
navigation:
  - class.mysql-xdevapi-databaseobject.md: « mysqlxdevapiDatabaseObject
  - mysql-xdevapi-databaseobject.getname.md: 'DatabaseObject::getName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-databaseobject.md: mysqlxdevapiDatabaseObject
title: 'DatabaseObject::existsInDatabase'
---
# DatabaseObject::existsInDatabase

(No version information available, might only be in Git)

DatabaseObject::existsInDatabase — Перевіряє, чи існує об'єкт у базі даних

### Опис

```methodsynopsis
abstract public mysql_xdevapi\DatabaseObject::existsInDatabase(): bool
```

Перевіряє, чи об'єкт бази даних посилається на об'єкт, який існує в базі даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо об'єкт існує в базі даних, інакше **`false`**, якщо це не так.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiDatabaseObject::existsInDatabase()****

```php
<?php

$existInDb = $dbObj->existsInDatabase();

?>
```
