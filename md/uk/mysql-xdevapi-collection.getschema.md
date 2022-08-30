Повертає об'єкт Schema

-   [« Collection::getOne](mysql-xdevapi-collection.getone.html)
    
-   [Collection::getSession »](mysql-xdevapi-collection.getsession.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiCollection](class.mysql-xdevapi-collection.html)
    
-   Повертає об'єкт Schema
    

# Collection::getSchema

(No version information available, might only be in Git)

Collection::getSchema — Повертає об'єкт Schema

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::getSchema(): Schema Object
```

Повертає об'єкт Schema, що містить колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Schema у разі успішного виконання або **`null`**, якщо об'єкт не може бути повернутий для цієї колекції.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::getSchema()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

var_dump($collection->getSchema());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(mysql_xdevapi\Schema)#9 (1) {
  ["name"]=>
  string(11) "addressbook"
}
```