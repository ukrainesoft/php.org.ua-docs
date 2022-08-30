Пропускає елементи

-   [« CollectionModify::set](mysql-xdevapi-collectionmodify.set.html)
    
-   [CollectionModify::sort »](mysql-xdevapi-collectionmodify.sort.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiCollectionModify](class.mysql-xdevapi-collectionmodify.html)
    
-   Пропускає елементи
    

# CollectionModify::skip

(No version information available, might only be in Git)

CollectionModify::skip — Пропускає елементи

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::skip(int $position): mysql_xdevapi\CollectionModify
```

Пропускає перші N елементів, які інакше було б повернуто операцією пошуку. Якщо кількість пропущених елементів перевищує розмір набору результатів, пошук повертає порожній набір.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`position`

Кількість елементів, що пропускаються.

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::skip()****

```php
<?php

$coll->modify('age > :age')->sort('age desc')->unset(['age'])->bind(['age' => 20])->limit(4)->skip(1)->execute();

?>
```