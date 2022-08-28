Отримує назву колекції

-   [« Collection::find](mysql-xdevapi-collection.find.html)
    
-   [Collection::getOne »](mysql-xdevapi-collection.getone.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Collection](class.mysql-xdevapi-collection.html)
    
-   Отримує назву колекції
    

# Collection::getName

(No version information available, might only be in Git)

Collection::getName — Отримує назву колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::getName(): string
```

Отримує назву колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва колекції у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::getName()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");


// ...

var_dump($collection->getName());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(6) "people"
```