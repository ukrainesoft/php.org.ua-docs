---
navigation:
  - class.mysql-xdevapi-crudoperationlimitable.md: « mysql\_xdevapi\\CrudOperationLimitable
  - class.mysql-xdevapi-crudoperationskippable.md: mysql\_xdevapi\\CrudOperationSkippable »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationlimitable.md: mysql\_xdevapi\\CrudOperationLimitable
title: 'CrudOperationLimitable::limit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CrudOperationLimitable::limit

(No version information available, might only be in Git)

CrudOperationLimitable::limit — Встановлює ліміт результату

### Опис

```methodsynopsis
abstract public mysql_xdevapi\CrudOperationLimitable::limit(int $rows): mysql_xdevapi\CrudOperationLimitable
```

Встановлює максимальну кількість записів або документів для повернення.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`rows`

Максимальна кількість записів чи документів.

### Значення, що повертаються

Об'єкт CrudOperationLimitable.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CrudOperationLimitable::limit()\*\*\*\*

```php
<?php

$res = $coll->find()->fields(['name as n','age as a','job as j'])->groupBy('j')->limit(11)->execute();
$res = $table->update()->set('age',69)->where('age > 15 and age < 22')->limit(4)->orderby(['age asc','name desc'])->execute();

?>
```
