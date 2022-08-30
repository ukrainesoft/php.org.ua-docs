Прив'язує значення до заповнювача

-   [« mysqlxdevapiCollectionRemove](class.mysql-xdevapi-collectionremove.html)
    
-   [CollectionRemove::construct »](mysql-xdevapi-collectionremove.construct.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiCollectionRemove](class.mysql-xdevapi-collectionremove.html)
    
-   Прив'язує значення до заповнювача
    

# CollectionRemove::bind

(No version information available, might only be in Git)

CollectionRemove::bind — Прив'язує значення до заповнювача

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::bind(array $placeholder_values): mysql_xdevapi\CollectionRemove
```

Прив'язує параметр до заповнювача за умови пошуку операції видалення.

Заповнювач має вигляд: NAME, де ':' - це загальний префікс, який повинен завжди вказаний перед будь-яким NAME, де NAME - це ім'я заповнювача. Метод bind приймає список заповнювачів, якщо за умови пошуку операції видалення необхідно замінити кілька об'єктів.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`placeholder_values`

Значення заповнювача для заміни за умови пошуку. Допускається використання кількох значень, які необхідно передати у вигляді масиву зіставлень PLACEHOLDERNAME->PLACEHOLDERVALUE.

### Значення, що повертаються

Об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionRemove::bind()****

```php
<?php

$res = $coll->remove('age > :age_from and age < :age_to')->bind(['age_from' => 20, 'age_to' => 50])->limit(7)->execute();

?>
```