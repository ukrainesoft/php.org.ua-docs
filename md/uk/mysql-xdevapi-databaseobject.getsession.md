---
navigation:
  - mysql-xdevapi-databaseobject.getname.md: '« DatabaseObject::getName'
  - class.mysql-xdevapi-docresult.md: mysqlxdevapiDocResult »
  - index.md: PHP Manual
  - class.mysql-xdevapi-databaseobject.md: mysqlxdevapiDatabaseObject
title: 'DatabaseObject::getSession'
---
# DatabaseObject::getSession

(No version information available, might only be in Git)

DatabaseObject::getSession — Отримує ім'я сесії

### Опис

```methodsynopsis
abstract public mysql_xdevapi\DatabaseObject::getSession(): mysql_xdevapi\Session
```

Отримує сесію, пов'язану з об'єктом бази даних.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Session.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiDatabaseObject::getSession()****

```php
<?php

$session = $dbObj->getSession();

?>
```
