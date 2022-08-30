Конструктор класу TableSelect

-   [« TableSelect::bind](mysql-xdevapi-tableselect.bind.html)
    
-   [TableSelect::execute »](mysql-xdevapi-tableselect.execute.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiTableSelect](class.mysql-xdevapi-tableselect.html)
    
-   Конструктор класу TableSelect
    

# TableSelect::construct

(No version information available, might only be in Git)

TableSelect::construct - Конструктор класу TableSelect

### Опис

private **mysqlxdevapiTableSelect::construct**

Об'єкт, який повертається методом select(); Використовуйте execute() для виконання запиту.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableSelect::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name','age')
  ->where('name like :name and age > :age')
  ->bind(['name' => 'John', 'age' => 42])
  ->orderBy('age desc')
  ->execute();

$row = $result->fetchAll();
print_r($row);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [name] => John
            [age] => 42
        )
)
```