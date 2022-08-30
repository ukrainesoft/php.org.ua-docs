Отримати схему таблиці

-   [« Table::getName](mysql-xdevapi-table.getname.html)
    
-   [Table::getSession »](mysql-xdevapi-table.getsession.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiTable](class.mysql-xdevapi-table.html)
    
-   Отримати схему таблиці
    

# Table::getSchema

(No version information available, might only be in Git)

Table::getSchema — Отримати схему таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::getSchema(): mysql_xdevapi\Schema
```

Витягти схему, пов'язану з таблицею.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Schema.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::getSchema()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->getSchema());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(mysql_xdevapi\Schema)#9 (1) {
  ["name"]=>
  string(11) "addressbook"
}
```