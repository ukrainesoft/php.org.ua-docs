---
navigation:
  - mysql-xdevapi-collectionremove.limit.md: '« CollectionRemove::limit'
  - class.mysql-xdevapi-columnresult.md: mysql\_xdevapi\\ColumnResult »
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.md: mysql\_xdevapi\\CollectionRemove
title: 'CollectionRemove::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionRemove::sort

(No version information available, might only be in Git)

CollectionRemove::sort — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::sort(string $sort_expr): mysql_xdevapi\CollectionRemove
```

Сортує набір результатів по полю, вибраному в аргументі sort\_expr. Дозволені напрямки: ASC (за зростанням) або DESC (за спаданням). Ця операція еквівалентна операції SQL 'ORDER BY' і відповідає тому ж набору правил.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`sort_expr`

Можна вказати один або кілька виразів сортування. Застосовується зліва направо, і кожен вираз розділяється комою.

### Значення, що повертаються

Об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CollectionRemove::sort()\*\*\*\*

```php
<?php

$res = $coll->remove('true')->sort('age desc')->limit(2)->execute();

?>
```
