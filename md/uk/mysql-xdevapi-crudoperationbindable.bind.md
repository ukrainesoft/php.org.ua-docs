---
navigation:
  - class.mysql-xdevapi-crudoperationbindable.md: « mysqlxdevapiCrudOperationBindable
  - class.mysql-xdevapi-crudoperationlimitable.md: mysqlxdevapiCrudOperationLimitable »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationbindable.md: mysqlxdevapiCrudOperationBindable
title: 'CrudOperationBindable::bind'
---
# CrudOperationBindable::bind

(No version information available, might only be in Git)

CrudOperationBindable::bind — Прив'язує значення до заповнювача

### Опис

```methodsynopsis
abstract public mysql_xdevapi\CrudOperationBindable::bind(array $placeholder_values): mysql_xdevapi\CrudOperationBindable
```

Прив'язує значення до певного наповнювача.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`placeholder_values`

Ім'я заповнювачів та значення для прив'язки.

### Значення, що повертаються

Об'єкт CrudOperationBindable.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCrudOperationBindable::bind()****

```php
<?php

$res = $coll->modify('name like :name')->arrayInsert('job[0]', 'Calciatore')->bind(['name' => 'ENTITY'])->execute();
$res = $table->delete()->orderby('age desc')->where('age < 20 and age > 12 and name != :name')->bind(['name' => 'Tierney'])->limit(2)->execute();

?>
```
