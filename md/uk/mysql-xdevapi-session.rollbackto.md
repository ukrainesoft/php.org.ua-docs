---
navigation:
  - mysql-xdevapi-session.rollback.md: '« Session::rollback'
  - mysql-xdevapi-session.setsavepoint.md: 'Session::setSavepoint »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::rollbackTo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::rollbackTo

(No version information available, might only be in Git)

Session::rollback To — Відкачує транзакцію до точки збереження

### Опис

```methodsynopsis
public mysql_xdevapi\Session::rollbackTo(string $name): void
```

Відкочує транзакцію до точки збереження.

### Список параметрів

`name`

Ім'я точки збереження для відкату; без урахування регістру.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::rollbackTo()\*\*\*\*

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("names");

$session->startTransaction();
$collection->add( '{"test1":1, "test2":2}' )->execute();

$savepoint1 = $session->setSavepoint();

$collection->add( '{"test3":3, "test4":4}' )->execute();

$savepoint2 = $session->setSavepoint();

$session->rollbackTo($savepoint1);
?>
```
