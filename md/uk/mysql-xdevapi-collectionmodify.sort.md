Встановлює критерії сортування

-   [« CollectionModify::skip](mysql-xdevapi-collectionmodify.skip.html)
    
-   [CollectionModify::unset »](mysql-xdevapi-collectionmodify.unset.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\CollectionModify](class.mysql-xdevapi-collectionmodify.html)
    
-   Встановлює критерії сортування
    

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

$res = $coll->modify('true')->sort('name desc', 'age asc')->limit(4)->set('Married', 'NO')->execute();

?>
```