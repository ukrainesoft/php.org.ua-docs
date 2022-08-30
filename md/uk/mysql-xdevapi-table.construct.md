Конструктор Table

-   [« mysqlxdevapiTable](class.mysql-xdevapi-table.html)
    
-   [Table::count »](mysql-xdevapi-table.count.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiTable](class.mysql-xdevapi-table.html)
    
-   Конструктор Table
    

# Table::construct

(No version information available, might only be in Git)

Table::construct — Конструктор Table

### Опис

private **mysqlxdevapiTable::construct**

Створити об'єкти таблиці.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");
?>
```