---
navigation:
  - mysql-xdevapi-databaseobject.getname.md: '« DatabaseObject::getName'
  - class.mysql-xdevapi-docresult.md: mysql\_xdevapi\\DocResult »
  - index.md: PHP Manual
  - class.mysql-xdevapi-databaseobject.md: mysql\_xdevapi\\DatabaseObject
title: 'DatabaseObject::getSession'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Session.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\DatabaseObject::getSession()\*\*\*\*

```php
<?php

$session = $dbObj->getSession();

?>
```
