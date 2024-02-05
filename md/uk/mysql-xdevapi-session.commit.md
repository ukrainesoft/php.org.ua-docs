---
navigation:
  - mysql-xdevapi-session.close.md: '« Session::close'
  - mysql-xdevapi-session.construct.md: 'Session::\_\_construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::commit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::commit

(PHP 4 >= 4.4.0, PHP 5, PHP 7, PHP 8)

Session::commit - Фіксує транзакцію

### Опис

```methodsynopsis
public mysql_xdevapi\Session::commit(): Object
```

Фіксує транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт SqlStatementResult.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::commit()\*\*\*\*

```php
<?php
$session    = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$collection = $session->getSchema("addressbook")->getCollection("friends");

$session->startTransaction();

$collection->add('{"John":42, "Sam":33}')->execute();
$savepoint = $session->setSavepoint();

$session->commit();
$session->close();
```
