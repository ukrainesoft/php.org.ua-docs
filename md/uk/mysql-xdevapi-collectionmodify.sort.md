---
navigation:
  - mysql-xdevapi-collectionmodify.skip.md: '« CollectionModify::skip'
  - mysql-xdevapi-collectionmodify.unset.md: 'CollectionModify::unset »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::sort

(No version information available, might only be in Git)

CollectionModify::sort — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::sort(string $sort_expr): mysql_xdevapi\CollectionModify
```

Сортує набір результатів за полем, переданим у аргументі sort\_expr. Дозволені напрямки сортування: ASC (за зростанням) або DESC (за спаданням). Ця операція еквівалентна операції SQL 'ORDER BY' і відповідає тому ж набору правил.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`sort_expr`

Можна вказати один або кілька виразів сортування. Оцінка виконується зліва направо, а вирази мають бути розділені комою.

### Значення, що повертаються

Повертає об'єкт класу CollectionModify, з яким можна працювати далі.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CollectionModify::sort()\*\*\*\*

```php
<?php

$res = $coll->modify('true')->sort('name desc', 'age asc')->limit(4)->set('Married', 'NO')->execute();

?>
```
