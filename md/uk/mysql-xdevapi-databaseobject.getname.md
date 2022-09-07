---
navigation:
  - mysql-xdevapi-databaseobject.existsindatabase.md: '« DatabaseObject::existsInDatabase'
  - mysql-xdevapi-databaseobject.getsession.md: 'DatabaseObject::getSession »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-databaseobject.md: mysqlxdevapiDatabaseObject
title: 'DatabaseObject::getName'
---
# DatabaseObject::getName

(No version information available, might only be in Git)

DatabaseObject::getName — Отримує ім'я об'єкта

### Опис

```methodsynopsis
abstract public mysql_xdevapi\DatabaseObject::getName(): string
```

Отримує ім'я об'єкта бази даних.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва об'єкта бази даних.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiDatabaseObject::getName()****

```php
<?php

$dbObjName = $dbObj->getName();

?>
```
