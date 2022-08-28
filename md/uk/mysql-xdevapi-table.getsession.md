Отримати таблицю сесій

-   [« Table::getSchema](mysql-xdevapi-table.getschema.html)
    
-   [Table::insert »](mysql-xdevapi-table.insert.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Table](class.mysql-xdevapi-table.html)
    
-   Отримати таблицю сесій
    

# Table::getSession

(No version information available, might only be in Git)

Table::getSession — Отримати таблицю сесій

### Опис

```methodsynopsis
public mysql_xdevapi\Table::getSession(): mysql_xdevapi\Session
```

Отримати сесію, пов'язану з таблицею.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Session.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::getSession()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

var_dump($table->getSession());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(mysql_xdevapi\Session)#9 (0) {
}
```