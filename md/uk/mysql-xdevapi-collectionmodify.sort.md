---
navigation:
  - mysql-xdevapi-collectionmodify.skip.md: '« CollectionModify::skip'
  - mysql-xdevapi-collectionmodify.unset.md: 'CollectionModify::unset »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysqlxdevapiCollectionModify
title: 'CollectionModify::sort'
---
# CollectionModify::sort

(No version information available, might only be in Git)

CollectionModify::sort — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::sort(string $sort_expr): mysql_xdevapi\CollectionModify
```

Сортує набір результатів по полю, вибраному в аргументі sortexpr. Дозволені напрямки: ASC (за зростанням) або DESC (за спаданням). Ця операція еквівалентна операції SQL 'ORDER BY' і відповідає тому ж набору правил.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`sort_expr`

Можна вказати один або кілька виразів сортування, Застосовується ліворуч, кожен вираз повинен бути розділений комою.

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::sort()****

```php
<?php

$res = $coll->modify('true')->sort('name desc', 'age asc')->limit(4)->set('Married', 'NO')->execute();

?>
```
