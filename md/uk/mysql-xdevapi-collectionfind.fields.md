Встановлює фільтр поля документа

-   [« CollectionFind::execute](mysql-xdevapi-collectionfind.execute.html)
    
-   [CollectionFind::groupBy »](mysql-xdevapi-collectionfind.groupby.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\CollectionFind](class.mysql-xdevapi-collectionfind.html)
    
-   Встановлює фільтр поля документа
    

# CollectionFind::fields

(No version information available, might only be in Git)

CollectionFind::fields — Встановлює фільтр поля документа

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::fields(string $projection): mysql_xdevapi\CollectionFind
```

Визначає шпальти для запиту, які потрібно повернути. Якщо не визначено, то повертаються усі стовпці.

### Список параметрів

`projection`

Може бути одним рядком або масивом рядків, ці рядки визначають стовпці, які мають бути повернені для кожного документа, який відповідає умові пошуку.

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::fields()****

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

// ...

$collection = $schema->getCollection("people");

$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->fields('name')
  ->execute();

var_dump($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  array(1) {
    ["name"]=>
    string(6) "Alfred"
  }
}
```