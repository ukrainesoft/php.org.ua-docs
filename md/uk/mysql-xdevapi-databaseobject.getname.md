---
navigation:
  - mysql-xdevapi-databaseobject.existsindatabase.md: '« DatabaseObject::existsInDatabase'
  - mysql-xdevapi-databaseobject.getsession.md: 'DatabaseObject::getSession »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-databaseobject.md: mysql\_xdevapi\\DatabaseObject
title: 'DatabaseObject::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DatabaseObject::getName

(No version information available, might only be in Git)

DatabaseObject::getName — Отримує ім'я об'єкта

### Опис

```methodsynopsis
abstract public mysql_xdevapi\DatabaseObject::getName(): string
```

Отримує ім'я бази даних.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва об'єкта бази даних.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\DatabaseObject::getName()\*\*\*\*

```php
<?php

$dbObjName = $dbObj->getName();

?>
```
