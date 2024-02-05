---
navigation:
  - mysql-xdevapi-session.sql.md: '« Session::sql'
  - class.mysql-xdevapi-sqlstatement.md: mysql\_xdevapi\\SqlStatement »
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::startTransaction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::startTransaction

(No version information available, might only be in Git)

Session::startTransaction - Починає транзакцію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::startTransaction(): void
```

Починає нову транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::startTransaction()\*\*\*\*

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
