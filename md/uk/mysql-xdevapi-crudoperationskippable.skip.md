---
navigation:
  - class.mysql-xdevapi-crudoperationskippable.md: « mysqlxdevapiCrudOperationSkippable
  - class.mysql-xdevapi-crudoperationsortable.md: mysqlxdevapiCrudOperationSortable »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationskippable.md: mysqlxdevapiCrudOperationSkippable
title: 'CrudOperationSkippable::skip'
---
# CrudOperationSkippable::skip

(No version information available, might only be in Git)

CrudOperationSkippable::skip — Кількість операцій для пропуску

### Опис

```methodsynopsis
abstract public mysql_xdevapi\CrudOperationSkippable::skip(int $skip): mysql_xdevapi\CrudOperationSkippable
```

Пропускає цю кількість записів у операції, що повертається.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`skip`

Кількість елементів, що пропускаються.

### Значення, що повертаються

Об'єкт CrudOperationSkippable.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCrudOperationSkippable::skip()****

```php
<?php

$res = $coll->find('job like \'Programmatore\'')->limit(1)->skip(3)->sort('age asc')->execute();

?>
```
