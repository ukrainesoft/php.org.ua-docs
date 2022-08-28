Встановлює критерії сортування

-   [« CollectionFind::offset](mysql-xdevapi-collectionfind.offset.html)
    
-   [mysql\_xdevapi\\CollectionModify »](class.mysql-xdevapi-collectionmodify.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\CollectionFind](class.mysql-xdevapi-collectionfind.html)
    
-   Встановлює критерії сортування
    

# CollectionFind::sort

(No version information available, might only be in Git)

CollectionFind::sort — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::sort(string $sort_expr): mysql_xdevapi\CollectionFind
```

Сортує набір результатів по полю, вибраному в аргументі sortexpr. Дозволені напрямки: ASC (за зростанням) або DESC (за спаданням). Операція еквівалентна операції SQL 'ORDER BY' і відповідає тому набору правил.

### Список параметрів

`sort_expr`

Можна вказати один або кілька виразів сортування, Застосовується ліворуч, кожен вираз повинен бути розділений комою.

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::sort()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");
$create
  ->add('{"name": "Alfred", "age": 18, "job": "Butler"}')
  ->execute();
$create
  ->add('{"name": "Reginald", "age": 42, "job": "Butler"}')
  ->execute();

// ...

$collection = $schema->getCollection("people");

$result = $collection
  ->find()
  ->sort('job desc', 'age asc')
  ->execute();

var_dump($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  [0]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b53610000000000000106"
    ["age"]=>
    int(18)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(6) "Alfred"
  }
  [1]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b53610000000000000107"
    ["age"]=>
    int(42)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(8) "Reginald"
  }
}
```