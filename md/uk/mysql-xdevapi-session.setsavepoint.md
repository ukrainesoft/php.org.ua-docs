---
navigation:
  - mysql-xdevapi-session.rollbackto.md: '« Session::rollbackTo'
  - mysql-xdevapi-session.sql.md: 'Session::sql »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::setSavepoint'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::setSavepoint

(No version information available, might only be in Git)

Session::setSavepoint — Створення точки збереження

### Опис

```methodsynopsis
public mysql_xdevapi\Session::setSavepoint(string $name = ?): string
```

Створює нову точку збереження транзакції.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`name`

Назва точки збереження. Ім'я генерується автоматично, якщо необов'язковий параметр `name` не визначено, як 'SAVEPOINT 1', 'SAVEPOINT 2' і т.д.

### Значення, що повертаються

Назва точки збереження.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::setSavepoint()\*\*\*\*

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
