---
navigation:
  - class.mysql-xdevapi-databaseobject.md: « mysql\_xdevapi\\DatabaseObject
  - mysql-xdevapi-databaseobject.getname.md: 'DatabaseObject::getName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-databaseobject.md: mysql\_xdevapi\\DatabaseObject
title: 'DatabaseObject::existsInDatabase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Приклад #1 Приклад використання** mysql\_xdevapi\\DatabaseObject::existsInDatabase()\*\*\*\*

```php
<?php

$existInDb = $dbObj->existsInDatabase();

?>
```
