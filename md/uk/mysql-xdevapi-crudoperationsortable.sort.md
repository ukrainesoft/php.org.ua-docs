---
navigation:
  - class.mysql-xdevapi-crudoperationsortable.md: « mysqlxdevapiCrudOperationSortable
  - class.mysql-xdevapi-databaseobject.md: mysqlxdevapiDatabaseObject »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationsortable.md: mysqlxdevapiCrudOperationSortable
title: 'CrudOperationSortable::sort'
---
# CrudOperationSortable::sort

(No version information available, might only be in Git)

CrudOperationSortable::sort — Сортує результати

### Опис

```methodsynopsis
abstract public mysql_xdevapi\CrudOperationSortable::sort(string $sort_expr): mysql_xdevapi\CrudOperationSortable
```

Сортує результуючий набір по полю, вибраному в аргументі sortexpr. Допустимий порядок сортування: ASC (за зростанням) або DESC (за спаданням). Ця операція еквівалентна операції SQL 'ORDER BY' і слідує тому ж набору правил.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`sort_expr`

Може бути надано один або кілька виразів сортування. Обчислення виконується зліва направо, і кожен вираз розділяється комою.

### Значення, що повертаються

Об'єкт CrudOperationSortable.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCrudOperationSortable::sort()****

```php
<?php

$res = $coll->find('job like \'Cavia\'')->sort('age desc', '_id desc')->execute();

?>
```
