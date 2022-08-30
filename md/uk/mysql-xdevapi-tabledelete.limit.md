Обмежує рядки для видалення

-   [« TableDelete::execute](mysql-xdevapi-tabledelete.execute.html)
    
-   [TableDelete::orderby »](mysql-xdevapi-tabledelete.orderby.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiTableDelete](class.mysql-xdevapi-tabledelete.html)
    
-   Обмежує рядки для видалення
    

# TableDelete::limit

(No version information available, might only be in Git)

TableDelete::limit — Обмежує рядки для видалення

### Опис

```methodsynopsis
public mysql_xdevapi\TableDelete::limit(int $rows): mysql_xdevapi\TableDelete
```

Встановлює максимальну кількість записів або документів для видалення.

### Список параметрів

`rows`

Максимальна кількість записів або документів для видалення.

### Значення, що повертаються

Об'єкт TableDelete.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableDelete::limit()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$table->delete()
  ->where("name = :name")
  ->bind(['name' => 'John'])
  ->orderby("age DESC")
  ->limit(1)
  ->execute();

?>
```