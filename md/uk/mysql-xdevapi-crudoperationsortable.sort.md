---
navigation:
  - class.mysql-xdevapi-crudoperationsortable.md: « mysql\_xdevapi\\CrudOperationSortable
  - class.mysql-xdevapi-databaseobject.md: mysql\_xdevapi\\DatabaseObject »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationsortable.md: mysql\_xdevapi\\CrudOperationSortable
title: 'CrudOperationSortable::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CrudOperationSortable::sort

(No version information available, might only be in Git)

CrudOperationSortable::sort — Сортує результати

### Опис

```methodsynopsis
abstract public mysql_xdevapi\CrudOperationSortable::sort(string $sort_expr): mysql_xdevapi\CrudOperationSortable
```

Сортує результуючий набір по полю, вибраному в аргументі sort\_expr. Допустимий порядок сортування: ASC (за зростанням) або DESC (за спаданням). Ця операція еквівалентна операції SQL 'ORDER BY' і слідує тому ж набору правил.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`sort_expr`

Може бути надано один або кілька виразів сортування. Обчислення виконується зліва направо, і кожен вираз розділяється комою.

### Значення, що повертаються

Об'єкт CrudOperationSortable.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CrudOperationSortable::sort()\*\*\*\*

```php
<?php

$res = $coll->find('job like \'Cavia\'')->sort('age desc', '_id desc')->execute();

?>
```
