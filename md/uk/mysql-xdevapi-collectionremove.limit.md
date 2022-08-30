Обмежує кількість документів для видалення

-   [« CollectionRemove::execute](mysql-xdevapi-collectionremove.execute.html)
    
-   [CollectionRemove::sort »](mysql-xdevapi-collectionremove.sort.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiCollectionRemove](class.mysql-xdevapi-collectionremove.html)
    
-   Обмежує кількість документів для видалення
    

# CollectionRemove::limit

(No version information available, might only be in Git)

Collection Remove::limit — Обмежує кількість документів для видалення

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::limit(int $rows): mysql_xdevapi\CollectionRemove
```

Встановлює максимальну кількість документів для видалення.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`rows`

Максимальна кількість документів видалення.

### Значення, що повертаються

Повертає об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionRemove::limit()****

```php
<?php

$res = $coll->remove('job in (\'Barista\', \'Programmatore\', \'Ballerino\', \'Programmatrice\')')->limit(5)->sort(['age desc', 'name asc'])->execute();

?>
```