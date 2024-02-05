---
navigation:
  - class.mysql-xdevapi-crudoperationbindable.md: « mysql\_xdevapi\\CrudOperationBindable
  - class.mysql-xdevapi-crudoperationlimitable.md: mysql\_xdevapi\\CrudOperationLimitable »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationbindable.md: mysql\_xdevapi\\CrudOperationBindable
title: 'CrudOperationBindable::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`placeholder_values`

Ім'я заповнювачів та значення для прив'язки.

### Значення, що повертаються

Об'єкт CrudOperationBindable.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CrudOperationBindable::bind()\*\*\*\*

```php
<?php

$res = $coll->modify('name like :name')->arrayInsert('job[0]', 'Calciatore')->bind(['name' => 'ENTITY'])->execute();
$res = $table->delete()->orderby('age desc')->where('age < 20 and age > 12 and name != :name')->bind(['name' => 'Tierney'])->limit(2)->execute();

?>
```
