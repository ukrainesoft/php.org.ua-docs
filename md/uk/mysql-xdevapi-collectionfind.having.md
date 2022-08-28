Встановлює умову для агрегатних функцій

-   [« CollectionFind::groupBy](mysql-xdevapi-collectionfind.groupby.html)
    
-   [CollectionFind::limit »](mysql-xdevapi-collectionfind.limit.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\CollectionFind](class.mysql-xdevapi-collectionfind.html)
    
-   Встановлює умову для агрегатних функцій
    

# CollectionFind::having

(No version information available, might only be in Git)

CollectionFind::having — Встановлює умову для агрегатних функцій

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::having(string $sort_expr): mysql_xdevapi\CollectionFind
```

Функція може бути використана після операції 'field', щоб зробити вибірку документів для вилучення.

### Список параметрів

`sort_expr`

Має бути коректний вираз SQL, дозволено використання агрегатних функцій.

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::having()****

```php
<?php

//Предполагая, что $coll является корректным объектом Collection

//Найти все документы, у которых 'age' больше 40,
//В объекте Result возвращаются только столбцы 'name' и 'age'.
$res = $coll->find()->fields(['name','age'])->having('age > 40')->execute();

?>
```