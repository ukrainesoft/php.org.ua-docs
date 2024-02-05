---
navigation:
  - class.mysql-xdevapi-crudoperationskippable.md: « mysql\_xdevapi\\CrudOperationSkippable
  - class.mysql-xdevapi-crudoperationsortable.md: mysql\_xdevapi\\CrudOperationSortable »
  - index.md: PHP Manual
  - class.mysql-xdevapi-crudoperationskippable.md: mysql\_xdevapi\\CrudOperationSkippable
title: 'CrudOperationSkippable::skip'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`skip`

Кількість елементів, що пропускаються.

### Значення, що повертаються

Об'єкт CrudOperationSkippable.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CrudOperationSkippable::skip()\*\*\*\*

```php
<?php

$res = $coll->find('job like \'Programmatore\'')->limit(1)->skip(3)->sort('age asc')->execute();

?>
```
