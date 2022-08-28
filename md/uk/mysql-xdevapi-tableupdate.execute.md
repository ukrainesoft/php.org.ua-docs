Виконує запит на оновлення

-   [« TableUpdate::\_\_construct](mysql-xdevapi-tableupdate.construct.html)
    
-   [TableUpdate::limit »](mysql-xdevapi-tableupdate.limit.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\TableUpdate](class.mysql-xdevapi-tableupdate.html)
    
-   Виконує запит на оновлення
    

# TableUpdate::execute

(No version information available, might only be in Git)

TableUpdate::execute — Виконує запит на оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::execute(): mysql_xdevapi\TableUpdate
```

Виконує затвердження оновлення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::execute()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$res = $table->update()
  ->set('level', 3)
  ->where('age > 15 and age < 22')
  ->limit(4)
  ->orderby(['age asc','name desc'])
  ->execute();

?>
```