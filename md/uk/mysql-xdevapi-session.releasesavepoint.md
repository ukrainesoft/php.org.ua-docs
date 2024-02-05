---
navigation:
  - mysql-xdevapi-session.quotename.md: '« Session::quoteName'
  - mysql-xdevapi-session.rollback.md: 'Session::rollback »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::releaseSavepoint'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::releaseSavepoint

(No version information available, might only be in Git)

Session::releaseSavepoint — Скасує встановлену точку збереження

### Опис

```methodsynopsis
public mysql_xdevapi\Session::releaseSavepoint(string $name): void
```

Скасує встановлену точку збереження.

### Список параметрів

`name`

Ім'я точки збереження для скасування.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::releaseSavepoint()\*\*\*\*

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("friends");

$session->startTransaction();
$collection->add( '{"test1":1, "test2":2}' )->execute();

$savepoint = $session->setSavepoint();

$collection->add( '{"test3":3, "test4":4}' )->execute();

$session->releaseSavepoint($savepoint);
$session->rollback();
?>
```
