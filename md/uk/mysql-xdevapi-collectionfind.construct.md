Конструктор класу CollectionFind

-   [« CollectionFind::bind](mysql-xdevapi-collectionfind.bind.html)
    
-   [CollectionFind::execute »](mysql-xdevapi-collectionfind.execute.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiCollectionFind](class.mysql-xdevapi-collectionfind.html)
    
-   Конструктор класу CollectionFind
    

# CollectionFind::construct

(No version information available, might only be in Git)

CollectionFind::construct - Конструктор класу CollectionFind

### Опис

private **mysqlxdevapiCollectionFind::construct**

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання CollectionFind**

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");
$result = $create
  ->add('{"name": "Alfred", "age": 18, "job": "Butler"}')
  ->execute();

// ...

$collection = $schema->getCollection("people");

$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->execute();

var_dump($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b536100000000000000cf"
    ["age"]=>
    int(18)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(6) "Alfred"
  }
}
```