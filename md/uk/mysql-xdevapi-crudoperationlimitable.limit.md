Встановлює ліміт результату

-   [« mysqlxdevapiCrudOperationLimitable](class.mysql-xdevapi-crudoperationlimitable.html)
    
-   [mysqlxdevapiCrudOperationSkippable »](class.mysql-xdevapi-crudoperationskippable.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiCrudOperationLimitable](class.mysql-xdevapi-crudoperationlimitable.html)
    
-   Встановлює ліміт результату
    

# CrudOperationLimitable::limit

(No version information available, might only be in Git)

CrudOperationLimitable::limit — Встановлює ліміт результату

### Опис

```methodsynopsis
abstract public mysql_xdevapi\CrudOperationLimitable::limit(int $rows): mysql_xdevapi\CrudOperationLimitable
```

Встановлює максимальну кількість записів або документів для повернення.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`rows`

Максимальна кількість записів чи документів.

### Значення, що повертаються

Об'єкт CrudOperationLimitable.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCrudOperationLimitable::limit()****

```php
<?php

$res = $coll->find()->fields(['name as n','age as a','job as j'])->groupBy('j')->limit(11)->execute();
$res = $table->update()->set('age',69)->where('age > 15 and age < 22')->limit(4)->orderby(['age asc','name desc'])->execute();

?>
```