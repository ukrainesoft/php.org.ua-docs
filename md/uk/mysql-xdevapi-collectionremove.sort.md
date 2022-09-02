---
navigation:
  - mysql-xdevapi-collectionremove.limit.md: '« CollectionRemove::limit'
  - class.mysql-xdevapi-columnresult.md: mysqlxdevapiColumnResult »
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.md: mysqlxdevapiCollectionRemove
title: 'CollectionRemove::sort'
---
# CollectionRemove::sort

(No version information available, might only be in Git)

CollectionRemove::sort — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::sort(string $sort_expr): mysql_xdevapi\CollectionRemove
```

Сортує набір результатів по полю, вибраному в аргументі sortexpr. Дозволені напрямки: ASC (за зростанням) або DESC (за спаданням). Ця операція еквівалентна операції SQL 'ORDER BY' і відповідає тому ж набору правил.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`sort_expr`

Можна вказати один або кілька виразів сортування. Застосовується зліва направо, і кожен вираз розділяється комою.

### Значення, що повертаються

Об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionRemove::sort()****

```php
<?php

$res = $coll->remove('true')->sort('age desc')->limit(2)->execute();

?>
```
