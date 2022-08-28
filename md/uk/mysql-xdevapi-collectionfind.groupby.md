Встановлює критерії угруповання

-   [« CollectionFind::fields](mysql-xdevapi-collectionfind.fields.html)
    
-   [CollectionFind::having »](mysql-xdevapi-collectionfind.having.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\CollectionFind](class.mysql-xdevapi-collectionfind.html)
    
-   Встановлює критерії угруповання
    

# CollectionFind::groupBy

(No version information available, might only be in Git)

CollectionFind::groupBy — Встановлює критерії угруповання

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::groupBy(string $sort_expr): mysql_xdevapi\CollectionFind
```

Функція може використовуватися для групування набору результатів ще по одному стовпцю, часто це використовується з агрегатними функціями, такими як COUNT,MAX,MIN,SUM і т.д.

### Список параметрів

`sort_expr`

Стовпець або стовпці, які повинні використовуватися для операції угруповання, це може бути один рядок, або масив рядкових аргументів, по одному для кожного стовпця.

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::groupBy()****

```php
<?php

//Предполагая, что $coll является корректным объектом Collection

//Извлекает все документы из коллекции и группирует результаты по полю 'name'
$res = $coll->find()->groupBy('name')->execute();

?>
```