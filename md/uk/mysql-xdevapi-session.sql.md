---
navigation:
  - mysql-xdevapi-session.setsavepoint.md: '« Session::setSavepoint'
  - mysql-xdevapi-session.starttransaction.md: 'Session::startTransaction »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::sql'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::sql

(No version information available, might only be in Git)

Session::sql — Створює SQL-запит.

### Опис

```methodsynopsis
public mysql_xdevapi\Session::sql(string $query): mysql_xdevapi\SqlStatement
```

Створює власний оператор SQL. Заповнювачі підтримуються нативним синтаксисом "?". Використовує метод `execute` до виконання затвердження SQL.

### Список параметрів

`query`

Твердження SQL для виконання.

### Значення, що повертаються

Об'єкт SqlStatement.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::sql()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("CREATE DATABASE addressbook")->execute();
?>
```
