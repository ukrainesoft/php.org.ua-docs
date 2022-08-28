Отримати таблицю схеми

-   [« Schema::getSession](mysql-xdevapi-schema.getsession.html)
    
-   [Schema::getTables »](mysql-xdevapi-schema.gettables.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Schema](class.mysql-xdevapi-schema.html)
    
-   Отримати таблицю схеми
    

# Schema::getTable

(No version information available, might only be in Git)

Schema::getTable — Отримати таблицю схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getTable(string $name): mysql_xdevapi\Table
```

Отримання об'єкта Table для зазначеної таблиці у схемі.

### Список параметрів

`name`

Ім'я таблиці.

### Значення, що повертаються

Об'єкт Table.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getTable()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->execute()->fetchAll();

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
    [1] => Array
        (
            [name] => Sam
            [age] => 33
        )
)
```