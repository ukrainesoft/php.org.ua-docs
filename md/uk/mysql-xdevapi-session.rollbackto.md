---
navigation:
  - mysql-xdevapi-session.rollback.md: '« Session::rollback'
  - mysql-xdevapi-session.setsavepoint.md: 'Session::setSavepoint »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysqlxdevapiSession
title: 'Session::rollbackTo'
---
# Session::rollbackTo

(No version information available, might only be in Git)

Session::rollbackTo — Відкачує транзакцію до точки збереження

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

**Приклад #1 Приклад використання **mysqlxdevapiSession::rollbackTo()****

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("names");

$session->startTransaction();
$collection->add( '{"test1":1, "test2":2}' )->execute();

$savepoint1 = $session->setSavepoint();

$collection->add( '{"test3":3, "test4":4}' )->execute();

$savepoint2 = $session->setSavepoint();

$session->rollbackTo($savepoint1);
?>
```
