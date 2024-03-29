---
navigation:
  - mysql-xdevapi-session.releasesavepoint.md: '« Session::releaseSavepoint'
  - mysql-xdevapi-session.rollbackto.md: 'Session::rollbackTo »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::rollback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::rollback

(No version information available, might only be in Git)

Session::rollback - Відкочує транзакцію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::rollback(): void
```

Відкочує транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::rollback()\*\*\*\*

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("names");

$session->startTransaction();
$collection->add( '{"test1":1, "test2":2}' )->execute();

$savepoint = $session->setSavepoint();

$collection->add( '{"test3":3, "test4":4}' )->execute();

$session->releaseSavepoint($savepoint);
$session->rollback();
?>
```
